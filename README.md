# Machine-Learning

# Linear Regression — Closed-Form vs Gradient Descent (from scratch)

This script fits a straight line to **synthetic data** and compares two solutions:

- **Closed-form (Normal Equation):** solves for θ analytically.
- **Gradient Descent (GD):** iteratively optimizes MSE to reach the same solution.

## What it does
- **Data:** 200 points from `y = 3 + 4x + ε` with `x ~ U(0,5)`, `ε ~ N(0,1)` (seeded).
- **Design matrix:** adds a bias column of ones for the intercept.
- **Closed-form:** `θ = (XᵀX)⁻¹ Xᵀ y` → prints `b` (intercept) and `w` (slope).
- **GD:** learning rate `η = 0.05`, `1000` iterations → tracks MSE loss; prints `b`, `w`, and parameter differences.
- **Plots:** 
  1) raw data + both fitted lines  
  2) GD **loss vs. iterations**

> In this well-conditioned setup, GD converges to (almost) the same parameters as the closed-form solution.

## Requirements
```bash
pip install numpy matplotlib
