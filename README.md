# Constrained Density Estimation

This repository contains the code and resources for the final project of the University of Washington's BIOST 527 course, titled "Density Estimation under Moment Constraints." The project explores and implements the Constrained Density Estimation method introduced by Hall and Presnell.

## Learning Objectives

The project has two primary objectives:
1. Understand the derivation of the Constrained Density Estimation method and improve the optimization technique.
2. Perform simulations of kernel density estimation with moment constraints.

## Repository Structure

- [project report](https://github.com/SZ-yang/BIOST527_ConstrainedKDE-/blob/main/BIOST527_FinalProject_ConstrainedDenistyEstimation.pdf)
- [code for simulation](https://github.com/SZ-yang/BIOST527_ConstrainedKDE-/blob/main/Constrained_KDE_Simulation.ipynb)
- [plots of the simulation](https://github.com/SZ-yang/BIOST527_ConstrainedKDE-/tree/main/plots)


## Abstract

The study aims to explore the Constrained Density Estimation method, focusing on moment constraints. The method employs a biased-bootstrap approach, where weights are optimized to satisfy specific constraints. We also improve the optimization technique by using the Gauss-Newton method with line search for better convergence.

## Methodology

### Bootstrap and Kernel Density Estimation
Kernel Density Estimation (KDE) is used as the base estimator. For KDE, we use the biweight kernel.

### Biased-Bootstrap
A weighted bootstrap method is used to adjust the weights to meet the moment constraints. The optimization problem is formulated to minimize the Kullback-Leibler divergence between the uniform and biased bootstrap distributions.

### Estimators and Constraints Linear in Probabilities
The constrained KDE is expressed as a linear combination of kernel functions, with constraints ensuring that specific sample moments are maintained.

### Optimization Problem
The optimization problem is solved using the Gauss-Newton method with line search to ensure convergence.

## Simulation

### Kernel and Test Setup
Simulations were conducted using an asymmetric bimodal normal mixture. Four tests were performed with different moment constraints: no constraints, first two moments constrained, first three moments constrained, and first four moments constrained.

### Simulation Results
The results demonstrate the effectiveness of the constrained estimation approach, with the mean square error (MSE) decreasing as more moment constraints are imposed.

## Results

The simulation results validate the theoretical benefits of the constrained density estimation method. Adding moment constraints systematically improves the accuracy of the density estimates, as reflected by the decreasing MSE values.

## Discussion

The project successfully met its learning objectives and improved upon Hall's original algorithm by adopting the Gauss-Newton method. The constrained estimation approach ensures that the estimated densities closely match the underlying distribution, which is beneficial for applications requiring precise density estimates.

## Acknowledgements

Special thanks to Professor Eardi Lila and TA Ethan Ancell for their support throughout the course. I would also like to honor the memory of Professor Peter Hall.

## References

1. Hall, P., DiCiccio, T. J., and Romano, J. P. On Smoothing and the Bootstrap. The Annals of Statistics, 1989.
2. Hall, P., and Presnell, B. Density estimation under constraints. Journal of Computational and Graphical Statistics, 1999.

## Usage

To run the simulations and generate the results, navigate to the `code/` directory and execute the provided scripts. Ensure that the necessary dependencies are installed.
