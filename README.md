# Unconstrained One-Dimensional Optimization Algorithms

This repository contains MATLAB implementations of three fundamental numerical optimization methods: **Bisection**, **Newton-Raphson**, and **Golden Section Search**. 

These scripts were developed to solve unconstrained one-dimensional optimization problems, specifically targeting the minimization of nonlinear functions.

## 📋 Table of Contents
- [Overview](#overview)
- [Problem Definition](#problem-definition)
- [Methods Implemented](#methods-implemented)
  - [1. Bisection Method](#1-bisection-method)
  - [2. Newton-Raphson Method](#2-newton-raphson-method)
  - [3. Golden Section Search](#3-golden-section-search)
- [Results](#results)
- [Usage](#usage)
- [Course Information](#course-information)

## 🔍 Overview
The primary goal of this project is to identify the minimum of a nonlinear objective function using both derivative-based and derivative-free techniques. The project compares the convergence behavior, speed, and robustness of each algorithm.

## 📉 Problem Definition
The specific test function used for validation across all methods is:

$$f(x) = (x-1)^2 (x-2) (x-3)$$

**Domain:** $0 \le x \le 4$  
**Target Minimum:** The algorithms aim to find the local minimum located at approximately $x \approx 2.6404$.

## ⚙️ Methods Implemented

### 1. Bisection Method
* **File:** `Bisection.m`
* **Type:** Derivative-based (Bracketing).
* **Logic:** Finds the stationary point where $f'(x) = 0$ by repeatedly halving the interval. Requires the derivative to change signs within the initial interval.
* **Pros:** Guaranteed convergence if the interval is chosen correctly.
* **Cons:** Slower (linear convergence) compared to Newton-Raphson.

### 2. Newton-Raphson Method
* **File:** `Newton-Raphson.m`
* **Type:** Derivative-based (Open Method).
* **Logic:** Uses both the first derivative $f'(x)$ and second derivative $f''(x)$ to approximate the function quadratically and jump closer to the root of the derivative.
* **Pros:** Extremely fast convergence (quadratic) near the optimum.
* **Cons:** Requires calculation of the second derivative; sensitive to the initial guess.

### 3. Golden Section Search
* **File:** `GoldenSection.m`
* **Type:** Derivative-free (Bracketing).
* **Logic:** Reduces the search interval iteratively using the Golden Ratio ($\tau \approx 0.618$). It evaluates the function values directly rather than derivatives.
* **Pros:** Robust; does not require the function to be differentiable; never diverges.
* **Cons:** Linear convergence (slower than Newton-Raphson).

## 📊 Results
All three methods successfully converged to the minimum point. A summary of performance based on the reports:

| Method | Convergence Speed | Derivative Required? | Final Result ($x_{opt}$) |
| :--- | :--- | :--- | :--- |
| **Newton-Raphson** | Fast (Quadratic) | Yes ($f', f''$) | ~2.6404 |
| **Bisection** | Moderate (Linear) | Yes ($f'$) | ~2.6404 |
| **Golden Section** | Moderate (Linear) | No | ~2.6404 |

## 🚀 Usage
To run these simulations:

1.  Ensure you have **MATLAB** installed.
2.  Clone this repository:
    ```bash
    git clone [https://github.com/your-username/repository-name.git](https://github.com/your-username/repository-name.git)
    ```
3.  Open MATLAB and navigate to the project folder.
4.  Run any of the scripts directly (e.g., `Newton-Raphson.m`). The scripts include the function definition and will output the iteration history to the command window.

## 🎓 Course Information
This work was conducted as part of the coursework for:
* **Course:** MEE445: Introduction to Artificial Neural Networks
* **Topic:** Numerical Optimization Techniques
* **Author:** Müslüm Can KANDAMAR

---
*This repository is for educational purposes.*