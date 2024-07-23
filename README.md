# Parallel-Monte-Carlo-Simulation-for-Pi-Calculation

Objective: Implement a Monte Carlo simulation to estimate the value of Pi using OpenMP.

Description: Monte Carlo simulations use random sampling to estimate mathematical results. The goal is to estimate Pi by randomly generating points in a unit square and counting how many falls within a quarter circle.

Steps:
1.	Implement the Monte Carlo simulation for Pi calculation in serial.
2.	Use OpenMP to parallelize the generation and counting of random points.
3.	Ensure thread safety when updating shared variables.
4.	Run the simulation with different numbers of points and threads to analyse the performance.
5.	Compare the accuracy and performance of the parallel implementation with the serial one.

Key Learning Outcomes:

•	Random number generation and statistical estimation.

•	Managing shared variables and thread safety.

•	Performance tuning for parallel simulations.


Main class explanation

Using the Monte Carlo method, the given C++ implementation calculates Pi's value. The main function invokes the calculatePi function to 
estimate Pi, specifies the number of points (numPoints) to generate for the simulation, seeds the random number generator with the 
current time, and prints the result. The calculatePi function creates a unit square with random points, determines if each point is 
inside a quarter circle, and then estimates Pi using the ratio of points inside the circle to all of the points.

