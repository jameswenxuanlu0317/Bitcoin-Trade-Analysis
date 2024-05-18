# Results
**Team Members:**
---
- Safeer Ahmed (sahme73)
- Thomas Alakkatt (talakk2)
- James Lu (jameslu2)
- Matt Casper (mcasper3)
---
**DFS**
---
**Outputs:** The output of the depth first search algorithm is a depth first search starting at a user specified node. Part of answering our leading question was finding the connected component of a certain user. Thus, if a particular user was found to be involved in some illicit activity, the nodes with which a user trades can be identified as potential accomplices. When running this on the dataset, we found that the users in our dataset were either not involved in any trades or involved in a network with the entire dataset.
___
**Tests:** To test our algorithm, we first utilized a basic graph we borrowed from the lecture notes. To ensure correctness, we added and subtracted different edges to make the traversal change. The traversal remained correct, so we concluded the algorithm worked. We next tested on a cycle graph to ensure the DFS properly terminated without running around the loop forever. Next, we tested that the overall DFS covered all components of a disconnected graph. We also tested a graph with some nodes that were involved in no trades to ensure they did not appear in our traversal. Finally, we tested that inputting an out of bounds value into the traversal as a start point doesn’t cause a crash.
___
**Dijkstra’s Algorithm**
---
**Outputs:** The output of running on the shortest path on our full scale dataset is the shortest weighted path between two user specified nodes. For example, if it is called from user 1 to user 1234, the output is 1, 174, 177, 7517, 159, 1234. This represents the least trustworthy path between the two users. This could answer our leading question by finding the least trusted method two users may be exchanging money. 
___
**Tests:** To test Dijkstra’s algorithm, we began by importing a graph directly from lecture and testing it from several start points to several endpoints. We also tested on the two cycle graphs from lecture where one has a very highly weighted edge and must go all the way around and the other can go directly there. We next tested what would happen if there was no path from start to finish but both were involved in the graph. Finally, we considered edge cases such as if either or both the start and end were invalid (negative numbers or out of bounds numbers) or if the nodes were involved in no trades, where the algorithm should run in constant time. Our edge cases test is titled “test worthless.”
___
**PageRank**
---
**Outputs:** The output of calling this on the entire dataset is the PageRank value of each node in the graph. The user may also call it for a specific user of interest to see only the PageRank value for that user. The PageRank value is defined as each rating given to that user divided by the total number of people that ranked that user. Effectively, this calculates the average score given to each user by all other users. We also state the users that average the maximum possible rating of 21 and those that average the lowest possible rating of 1. Interestingly, we found, many users average a rating of 12-13. Note that a score of 0 means that the user was never rated.
___
**Tests:** To test PageRank, we simply performed it a number of times on a variety of graphs. First, we called the individual one on a simple, small graph. Next, we tested whether calling PageRank on a graph with a number of connected components would output the proper results. Next, we tested that PageRank single did not crash on a graph where some nodes were not rated. We then tested PageRank all on a graph to ensure that it performed as expected. Finally, we tested edge cases of inputting invalid inputs (negative numbers and out of bounds values) into PageRank single to ensure it did not crash and returned -1 as expected.
___
**Answer to the Leading Question**
---
The DFS answered something that was inherently a part of our leading question. It found that the dataset, rather than containing multiple disjoint components, contained one large component where any involved node was accessible from any other node. Thus, this dataset represents only one trading network. Using PageRank all, we were able to answer our leading question of which nodes were most and least trustworthy. The nodes that averaged the highest score were users 414, 418, 776, 782, 788, 789, 790, 791, 794, 795, 797, 805, 806, 808, 811, 814, 819, 820, 823, 827, 828, 829, 831, 833, 834, 835, 836, 837, and 838. The nodes with the lowest rating were users 7448, 7449, 7450, 7452, 7453, 7454, 7455, 7456, 7457, 7458, 7459, 7460, 7461, 7462, 7463, 7464, 7465, 7466, 7467, 7468, 7469, 7470, 7471, 7472, 7473, 7474, 7475, 7476, 7477, 7478, 7479, 7480, 7481, 7533, 7534, 7537, 7538, 7539, 7541, 7542, 7543, 7545, 7572, 7573, 7574, 7587, 7592, and 7597. Interestingly, the nodes with the lowest scores seem to be concentrated at the highest user IDs, while the nodes with the highest scores seem to be on the lower end. Also, we noticed that a vast majority of the nodes tend to average a rating of 12-13, meaning that most users are not deemed trustworthy.
