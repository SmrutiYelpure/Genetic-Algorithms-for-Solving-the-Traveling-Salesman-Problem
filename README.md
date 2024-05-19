<h1>Genetic Algorithms for Solving the Traveling Salesman Problem</h1>
<p>This project aims to solve the Traveling Salesman Problem (TSP) using various genetic algorithms. The TSP is a well-known combinatorial optimization problem in computer science and operations research. Given a list of cities and the distances between each pair of cities, the objective is to find the shortest possible route that visits each city exactly once and returns to the starting city.</p>
<p>Genetic algorithms are a class of evolutionary algorithms inspired by the process of natural selection. They are widely used for solving complex optimization problems like the TSP, where the search space is vast, and finding the optimal solution using traditional methods becomes computationally expensive or even intractable.</p>
<h2>Table of Contents</h2>
<ul>
  <li><a href="#prerequisites">Prerequisites</a></li>
  <li><a href="#dataset">Dataset</a></li>
  <li><a href="#implementation">Implementation</a></li>
  <li><a href="#usage">Usage</a></li>
  <li><a href="#contributing">Contributing</a></li>
  <li><a href="#license">License</a></li>
</ul>
<h2 id="prerequisites">Prerequisites</h2>
<p>To run this project, you'll need the following dependencies installed:</p>
<ul>
  <li>Python 3.x</li>
  <li>NumPy (for numerical operations)</li>
  <li>Matplotlib (for visualizing the tours)</li>
</ul>
<p>You can install the required dependencies using pip:</p>
<pre><code>pip install numpy matplotlib</code></pre>
<h2 id="dataset">Dataset</h2>
<p>The project includes functions to generate random datasets containing city coordinates. The datasets are saved as text files with the following naming convention:</p>
<ul>
  <li><code>dataset_42.txt</code> (containing coordinates for 42 cities)</li>
  <li><code>dataset_512.txt</code> (containing coordinates for 512 cities)</li>
  <li><code>dataset_662.txt</code> (containing coordinates for 662 cities)</li>
</ul>
<p>Each line in the dataset file represents the coordinates of a city in the format <code>x y</code>, where <code>x</code> and <code>y</code> are floating-point numbers within a specified range (0-100 by default).</p>
<p>You can modify the dataset generation functions to customize the range or distribution of city coordinates, or even load datasets from external sources.</p>
<h2 id="implementation">Implementation</h2>
<p>The project implements the following components:</p>
<ol>
  <li><strong>Dataset Generation</strong>: Functions to generate random city coordinates and save them to files.</li>
  <li><strong>Genetic Algorithm</strong>: The main genetic algorithm implementation, which includes functions for initialization, selection, crossover, mutation, and fitness evaluation. The implemented techniques are:
    <ul>
      <li><strong>Selection</strong>: Tournament selection is used to select individuals (candidate solutions) for reproduction based on their fitness values.</li>
      <li><strong>Crossover</strong>: Ordered crossover is employed to combine the genetic information of two parent individuals to produce offspring.</li>
      <li><strong>Mutation</strong>: Swap mutation is applied to introduce diversity in the population by randomly swapping the positions of two cities in a tour.</li>
    </ul>
  </li>
  <li><strong>TSP Solver</strong>: A function that encapsulates the genetic algorithm and provides the solution for the TSP instances. It evolves a population of candidate solutions over multiple generations, applying selection, crossover, and mutation operations to find the best individual (tour) that minimizes the total distance traveled.</li>
  <li><strong>Visualization</strong>: A function to visualize the best tour found by the genetic algorithm using the Matplotlib library. This helps to visually inspect the quality of the obtained solution.</li>
</ol>
<h2 id="usage">Usage</h2>
<p>To run the project, follow these steps:</p>
<ol>
  <li>Clone the repository or download the source code.</li>
  <li>Install the required dependencies (NumPy and Matplotlib).</li>
  <li>Run the script (<code>python script.py</code>).</li>
</ol>
<p>The code will generate random datasets, save them to files, and then solve the TSP for each dataset using the genetic algorithm. The best tours and total distances will be printed to the console, and the best tour for the 42 city instance will be visualized using Matplotlib.</p>
<p>You can adjust various parameters of the genetic algorithm, such as population size, number of generations, and mutation rate, by modifying the corresponding variables in the code. These parameters can have a significant impact on the performance and convergence of the algorithm.</p>
<p>Additionally, you can experiment with different genetic operators (e.g., different selection, crossover, or mutation techniques) or incorporate advanced techniques like elitism or local search to potentially improve the quality of the solutions obtained.</p>
<h2 id="contributing">Contributing</h2>
<p>Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please open an issue or submit a pull request on the project's GitHub repository.</p>
<p>Some potential areas for contribution include:</p>
<ul>
  <li>Implementing additional genetic operators or optimization techniques</li>
  <li>Enhancing the visualization capabilities</li>
  <li>Adding support for loading datasets from external sources</li>
  <li>Parallelizing the genetic algorithm for improved performance</li>
  <li>Extending the project to solve other variants of the TSP or related problems</li>
</ul>
<h2 id="license">License</h2>
<p>This project is licensed under the <a href="LICENSE">MIT License</a>.</p>
