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


Project Explanation 

The goal of this project is to use OpenMP to parallelize and serialize the Monte Carlo method for estimating the value of Pi. The Monte 
Carlo method is a statistical method that makes use of random sampling to address potentially deterministic mathematical issues. Through
the usage of OpenMP, efficiency will be improved by dividing the computation over several threads, enabling rapid and more effective 
calculation completion.


Main class Explanation

Using the Monte Carlo method, the given C++ implementation calculates Pi's value. The "main" function invokes the "calculatePi" function
to estimate Pi, specifies the number of points ("numPoints") to generate for the simulation, seeds the random number generator with the 
current time, and prints the result. The "calculatePi" function creates a unit square with random points, determines if each point is 
inside a quarter circle, and then estimates Pi using the ratio of points inside the circle to all of the points.

Parallel Version Class Explanation 

In this instance, the given C++ application uses OpenMP for parallel processing along with the Monte Carlo approach to estimate the 
value of Pi. Using parallel threads, the "calculatePi" function creates random points inside a unit square and determines if each point
is inside a quarter circle. To guarantee diverse random values, the random number generator is seeded differently for each thread. The 
count of points inside the circle is correctly accumulated across all threads thanks to the "#pragma omp for reduction(+:insideCircle)"
directive. The primary function calls "calculatePi", sets the number of points, seeds the random number generator, and outputs the 
estimated Pi value. This parallel strategy makes use of several CPU cores in an effort to increase performance.


                                                Parallel_Version_Performance_Measurement to Parallel_Version

- The purpose of the code is a Monte Carlo method to estimate the value of the number 𝜋.
* Using parallel computing, to speed up the process of generating + checking the number of random points.
  • The code utilises the parallel computing capabilities of OpenMP.
    By splitting the task into multiple threads, we want to reduce the execution time of the programme.
• The Monte Carlo method applied here is our tool for numerical modelling.


                                                     Parallel_Version_Threads_Configuration

- The purpose of this code is to demonstrate the use of the Monte Carlo method to estimate the value of the number 𝜋.
• Parallel region: Inside #pragma omp parallel, a parallel region is created where each thread executes a different copy of the code.
 Within this territory/region, random numbers are generated for each thread.
• Parallel loop: The #pragma omp for reduction(+:insideCircle) directive distributes loop data between threads and sums the values of the insideCircle variable from all threads.

• The value of π is estimated based on the ratio of points that fell inside the quarter circle to the total number of points generated.
 The result is multiplied by 4 because we are working with a quarter circle.
- So this code demonstrates the use of OpenMP to perform calculations in parallel while reducing the program execution time too.
  We also specify the number of threads using omp_set_num_threads, which allows us to control parallel execution.
