## _Bitcoin Alpha Analysis Project_

### Final Presentation

Link to final presentation: https://youtu.be/qs5qq15pCMU

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#github-organization">Organization</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a>
      <ul>
        <li><a href="#example">Example</a></li>
      </ul>
    </li>
    <li>
      <a href="#contributors">Contributors</a>
    </li>
  </ol>
</details>

<!-- GETTING STARTED -->
## Getting Started

To setup the project locally, follow the installation instructions below.

### GitHub Organization

In the main repository the team contract, project proposal, final written report (in results.md), and log can be found. Our final presentation can be found at https://youtu.be/qs5qq15pCMU. All of the code for this project is contained in the project folder. Within the project folder, all header files can be found in the include folder. The majority of our code (.cpp files) can be found in the src folder. All data is in the data folder. The test cases are in the tests folder. All files that are necessary to run catch are found in the catch folder. The executable files, once compiled using the appropriate commands, can be found in the bin folder.

<p align="right">(<a href="#top">back to top</a>)</p>

### Installation

1. Clone the repo in your desired directory
   ```sh
   git clone https://github-dev.cs.illinois.edu/cs225-sp22/talakk2-sahme73-jameslu2-mcasper3.git
   ```
2. Change directory to project folder
   ```sh
   cd project
   ```
   
NOTE: The following line is sometimes needed if running on an EWS machine is causing issues!
    ```sh
    module load llvm/6.0.1
    ```

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

To utilize the codebase of the project, follow the instructions below:

<br></br>

_Running the main executable:_
1. Make the main executable
   ```sh
   make exec
   ```
2. Run the main executable
   ```sh
   ./bin/exec
   ```

<br></br>

_Running the test executables:_
1. Make the tests executable
   ```sh
   make tests
   ```
2. Run the tests executable
   ```sh
   ./bin/tests
   ```

<br></br>

_Cleaning the /bin/ directory:_
1. Clean the directory
   ```sh
   make clean
   ```

<p align="right">(<a href="#top">back to top</a>)</p>

### Example

Running Main:
After running main, you will be prompted messages in the terminal to properly execute the algorithms. The prompts will also guide the user to determine what inputs are accepted or not. All resulting outputs will be displayed in the terminal of choice (where the run commands are executed from).

Running Tests:
To test only one algorithm, run `./bin/tests [part=num]`, but replace num with the part you wish to test: 
1- Data cleaning and graph building.
2- DFS
3- Dijkstra’s Shortest Path Algorithm
4- PageRank Algorithm

<p align="right">(<a href="#top">back to top</a>)</p>

## Contributors
- Safeer Ahmed (sahme73)
- Thomas Alakkatt (talakk2)
- James Lu (jameslu2)
- Matt Casper (mcasper3)

<p align="right">(<a href="#top">back to top</a>)</p>
