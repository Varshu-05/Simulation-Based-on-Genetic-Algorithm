# Simulation-Based-on-Genetic-Algorithm
This project is a 2D evolutionary simulation where two species—Prey and Predators—co-evolve in a shared environment. Each agent is controlled by a custom-built Neural Network that processes visual data and determines movement. Through a Genetic Algorithm, the agents learn over generations: prey learn to avoid capture, and predators learn to hunt more efficiently. 

# Neural-Evolution Simulation
A Python-based simulation demonstrating the power of Neuroevolution. Agents interact in a survival-of-the-fittest environment, where their "brains" (Neural Networks) are optimized over time using a Genetic Algorithm.

# Technical Architecture
1. Neural Network
   Input Layer: 36 neurons representing a $360^\circ$ field of vision (split into $10^\circ$ sectors).
   Hidden Layer: A single dense layer with 200 neurons using the Sigmoid activation function.
   Output Layer: 9 neurons corresponding to movement directions (N, NE, E, SE, S, SW, W, NW, and Idle).
   Matrix Math: Built entirely using NumPy for efficient dot products and weight manipulations.
   
2.The Genetic Algorithm (GA)
  Fitness Function: * Prey: Earn fitness based on survival time.
  Predators: Earn fitness based on the number of prey consumed.
  Selection: Uses Stochastic Universal Sampling (probability based on fitness) to select parents for the next generation.
  Mutation: Random weights are perturbed by a value between $[-0.5, 0.5]$ to introduce behavioral diversity and explore new strategies.
  Inheritance: Offspring inherit the weight matrices of their parents, ensuring successful traits are passed down.
