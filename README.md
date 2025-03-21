# Multiple Linear Regression Project 📊✏️

## Overview
This repository contains our implementation and analysis for the Multiple Linear Regression project. The project is divided into several parts: a theoretical derivation of the optimal regression solution, practical exercises with synthetic datasets, and an application to real-world data from the Real Estate Valuation Data Set. Our work details every matrix and vector operation used in the derivation, as well as the estimation, evaluation, and visualization of regression models.

**Team Members:**
- Luca Mazzarello
- Ignacio Pardo

## Table of Contents
1. [Part One: Theoretical Foundations](#part-one-theoretical-foundations)
   - Subspaces and Vector Spaces
   - Dot Product Identity
   - Derivation of the Orthogonality Condition
   - Derivation of the Normal Equations
   - Optimal Solution Formula
2. [Part Two: Regression in ℝ²](#part-two-regression-in-ℝ²)
   - Exercise 1: Plotting and Approximating Points
   - Exercise 2: Regression with Shifted Data and Model Extension
3. [Part Three: Real-World Application](#part-three-real-world-application)
   - Data Splitting: Training and Test Sets
   - Parameter Estimation and Response Prediction
   - Calculation of Mean Squared Error (MSE)
   - Error Visualization per House
   - Impact of Adding a Construction Year Feature
4. [Conclusions](#conclusions)
5. [References](#references)

## Part One: Theoretical Foundations
In this section, we derive the optimal solution **β\*** for the linear regression problem:

- **Subspaces and Vector Spaces:**  
  We show that the column space of the design matrix **X** is a subspace of ℝⁿ.

- **Dot Product Identity:**  
  Demonstrated that for column vectors, the dot product can be computed as  
  `u ⋅ v = vᵀu`.

- **Orthogonality Condition:**  
  By projecting **y** (the dependent variable vector) onto the subspace **S = {Xβ : β ∈ ℝᵖ}**, we derive the condition:  
  `Xᵀ(y - Xβ*) = 0`.

- **Normal Equations and Optimal Solution:**  
  Assuming the columns of **X** are linearly independent, we arrive at the normal equations:  
  `XᵀXβ* = Xᵀy`  
  which gives the closed-form solution:  
  `β* = (XᵀX)⁻¹Xᵀy`.

## Part Two: Regression in ℝ²
This part applies the theory to simple two-dimensional data:

- **Exercise 1:**  
  - **(a)** Plot the data points from `ejercicio_1.csv`.
  - **(b)** Compute the best-fit line using the normal equations and visualize the regression line.
  - **(c)** Re-plot the data after shifting the y-values by 12 units. Analyze the fit and discuss the problem.
  - **(d)** Discuss extending the model by including a column of 1's to approximate any line in the plane.

- **Exercise 2:**  
  - **(a)** Plot and approximate the points from `ejercicio_2.csv`.
  - **(b)** Discuss the suitability of the regression approximation when using these points for predictive purposes (e.g., forecasting processor temperature) and identify potential issues.

## Part Three: Real-World Application
Using the Real Estate Valuation Data Set from the UCI Machine Learning Repository:

- **Data Splitting:**  
  The dataset (414 houses) is split into training (observations 1–315) and test sets (observations 316–414).

- **Parameter Estimation:**  
  Estimate **β̂** that minimizes the Mean Squared Error (MSE) on the training data.

- **Response Prediction:**  
  Compute the predicted response vector **ŷ** and calculate the MSE on both training and test sets.

- **Error Analysis:**  
  Visualize the absolute errors per house. Notice that the error tends to be higher for more expensive houses.

- **Feature Extension:**  
  Evaluate the impact of adding a new feature (year built) and discuss why collinearity can negatively affect the MSE.

## Conclusions
- The theoretical derivation confirms that the optimal regression parameters can be obtained via the normal equations.
- Experiments in ℝ² demonstrate the importance of including an intercept (column of ones) to capture any line in the plane.
- The application to real-world data shows that our regression model performs well on test data (lower MSE) and provides valuable insights through error visualization.
- Adding redundant features (e.g., construction year computed from transaction date and house age) increases MSE due to collinearity.

## References
- [Real Estate Valuation Data Set](https://archive.ics.uci.edu/ml/datasets/Real+estate+valuation+data+set)
- Additional course materials and lecture notes.

Happy modeling and analysis! 📈🔍
