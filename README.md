# student_marks_prediction_ML
Student Marks Predictor built from scratch using Multiple Linear Regression, Gradient Descent, Feature Engineering, Polynomial Regression, and Z-Score Normalization with NumPy.
# Student Marks Predictor using Linear Regression

## Overview

This project predicts student marks using Multiple Linear Regression built completely from scratch using NumPy.

The project was made to understand how Machine Learning actually works internally.

It includes:
- Gradient Descent
- Cost Function
- Feature Engineering
- Polynomial Regression
- Z-Score Normalization
- Prediction System
- Visualization using Matplotlib

---

# Features Used

The model predicts marks using:

- Study Hours
- Attendance
- Scholarship Score
- Study Hours² (Polynomial Feature)

The squared feature was added to help the model capture curved/non-linear relationships instead of only straight-line predictions so that the predictions are accurate.

---

---

# Concepts Implemented

## 1. Linear Regression

The model learns relationships between student-related features and marks.

---

## 2. Gradient Descent

Gradient Descent is used to update weights and bias iteratively to reduce prediction error.

---

## 3. Cost Function

Mean Squared Error (MSE) was used to calculate how far predictions are from actual values.

---

## 4. Feature Engineering

A new feature study_hours²  was added to improve prediction capability.

---

## 5. Polynomial Regression

By adding squared study hours, the model can learn curved relationships instead of only linear ones.

---

## 6. Z-Score Normalization

Feature scaling was applied to improve convergence speed and stabilize gradient descent.

Formula used:

X_norm = (X - μ) / σ

---

# Dataset

![image.png](attachment:18307ff5-3f22-4589-b94e-46ae816b7598:image.png)

---

---

# Functions Implemented

## Prediction Function

Uses vectorized dot product for prediction.

predict(w, x, b)

---

## Cost Function

Calculates Mean Squared Error.

cost_fn(x, y, w, b)

---

## Gradient Function

Calculates gradients for:
- weights
- bias

gradient(x, y, w, b)

---

## Gradient Descent

Optimizes weights and bias over iterations.

gradient_descent(x,y,w,b,num_iters,cost_fn,alpha,gradient)

---

## Z-Score Normalization

Normalizes features before training.

zscore_normalization(x)

---

# Training Process

## Initial Parameters

w_initial = np.zeros(4)
b_initial = 0

## Alpha Value

For non-normalized data:

alpha = 6e-7

For normalized data:

alpha = 1e-2

Normalization allowed the model to use a much larger learning rate without exploding costs.

## Iterations

iterations = 1000

---

# Visualizations

The project generates:

- Cost vs Iterations graph

![image.png](attachment:fe6d1f12-4ed2-4e1f-969c-e34f90f23a5f:image.png)

- Feature distributions before normalization and after normalizaiton

![image.png](attachment:a38c33e2-19c1-4bf0-8265-6a77629a51e5:image.png)

- Prediction vs Target plots

![image.png](attachment:9452d578-3e83-4b9c-8807-d7dee724919d:image.png)

These graphs help analyze:
- convergence
- feature scaling effects
- prediction quality

---

# Sample Output

![image.png](attachment:dae6b2b1-4ab2-44d8-929a-05d00fbc8eef:image.png)

Actual Target value: 40

---

# Input Prediction System

The user can manually enter:

- Study Hours
- Attendance
- Scholarship

The program:
1. Creates polynomial feature
2. Normalizes input
3. Predicts marks using trained weights

---

# What I Learned

Through this project I learned:

- How gradient descent works internally
- Why feature scaling matters
- How polynomial regression improves predictions
- How vectorized prediction works using NumPy
- How learning rate affects convergence
- How to debug ML models

---
