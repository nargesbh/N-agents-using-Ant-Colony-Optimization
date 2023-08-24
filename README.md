# Ant Colony Optimization for Job Assignment

This repository contains Python code for solving the job assignment problem using Ant Colony Optimization (ACO). In this problem, a set of jobs needs to be assigned to a set of employees in such a way that the total cost is minimized. The ACO algorithm is used to find an optimal or near-optimal assignment of jobs to employees.

## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [Algorithm](#algorithm)
- [Code Structure](#code-structure)
- [Results](#results)
- [Parameters](#parameters)

## Introduction

The job assignment problem is a common optimization problem where you have a set of jobs and a set of employees, and you need to assign each job to one employee while minimizing a cost or objective function. In this repository, we use the Ant Colony Optimization (ACO) algorithm to find an optimal or near-optimal assignment.

## Usage

To use this code for solving the job assignment problem, follow these steps:

1. Clone the repository to your local machine:

```
git clone https://github.com/your-username/your-repo.git
```

2. Install the required libraries (NumPy) if you haven't already:

   ```
   pip install numpy
   ```

3. Modify the input file `jobX.assign` (where X is the job number) to represent your specific job assignment problem. Each line of the input file should contain the cost of assigning a job to an employee. check HW3.pdf file to access different examples.

4. In the code, set the parameters such as the number of ants, alpha, beta, learning rate, and evaporation rate based on your problem and preferences.

5. Run the code with the chosen input file and parameters.

## Algorithm

The Ant Colony Optimization (ACO) algorithm is a metaheuristic inspired by the foraging behavior of ants. In this context, ants represent candidate solutions (assignments of jobs to employees), and they construct solutions while stochastically moving through the solution space. The pheromone matrix is used to guide the ants towards better solutions, and it is updated based on the quality of the solutions found.

Here's a brief overview of the main components of the ACO algorithm used in this code:

- **Ants**: Ants are represented as arrays, with each index corresponding to an employee and the value at each index representing the job assigned to that employee.

- **Next Move**: Ants construct solutions by selecting the next job to assign to an employee. The probability of selecting a job is based on a combination of pheromone levels and a heuristic measure.

- **Cost Function**: A cost function is used to evaluate the quality of each ant's solution. Lower costs indicate better solutions.

- **Evaporation**: After each generation, the pheromone matrix is updated by evaporating some of the pheromone, preventing convergence to local optima.

## Code Structure

The code is structured as follows:

- `next_move`: Function to determine the next job to assign to an employee based on pheromone levels and a heuristic measure.

- `cost_function`: Function to calculate the cost of a given assignment.

- `evaporate`: Function to update the pheromone levels by evaporating some of the pheromone.

- `input_read`: Function to read the input from the specified file.

- `generation_maker`: Function to create a generation of ants with random initial assignments.

- `main`: The main function that runs the ACO algorithm to find an optimal or near-optimal assignment of jobs to employees.

## Results

The code has been tested on various job assignment problems (`job1.assign`, `job2.assign`, `job3.assign`, `job4.assign`, and `job5.assign`) with different parameters. Each job assignment problem may require tuning the parameters to achieve the best results. Below are some example results:

- **Job 1**: Found cost: 26, Optimal assignment: [3, 1, 2, 0]

- **Job 2**: Found cost: 332, Optimal assignment: [many assignments]

- **Job 3**: Found cost: 741, Optimal assignment: [many assignments]

- **Job 4**: Found cost: 21262, Optimal assignment: [many assignments]

- **Job 5**: Found cost: 57505, Optimal assignment: [many assignments]

Please note that the results may vary based on the specific input and parameters chosen.

## Parameters

To achieve the best results for your specific job assignment problem, you can adjust the following parameters in the code:

- `ant_num`: The number of ants in each generation.

- `alpha`: A parameter controlling the influence of pheromone levels on ant decisions.

- `beta`: A parameter controlling the influence of heuristic information on ant decisions.

- `L_rate`: The learning rate, which determines how much pheromone is added.


