# Polynomial Regression Assignment (MS2026012)

This repository contains my solution to Assignment 1 (Polynomial Regression). The goal is to predict the target `y` for two datasets using polynomial regression only.

## Final models

- var1: all 6 inputs (x1-x6), polynomial degree 4
- var2: all 3 inputs (x1-x3), polynomial degree 8

## Method

- Expanded the inputs into polynomial features and standardised them.
- Fitted a linear regression on the expanded features.
- Chose the degree with 5-fold cross-validation, picking the degree with the lowest cross-validation MSE.
- Compared models that use fewer inputs to check that every input matters.
- Retrained on the full training data and predicted the test files.

## Files

- `polynomial_regression_MS2026012.ipynb` - the code (training, degree search, predictions)
- `MS2026012_train_var1.csv`, `MS2026012_test_var1.csv`, `MS2026012_train_var2.csv`, `MS2026012_test_var2.csv` - the datasets
- `MS2026012_pred_var1.csv`, `MS2026012_pred_var2.csv` - my predictions for the test sets

## How to run

Open the notebook in Google Colab, upload the four dataset CSV files, and choose **Runtime → Run all**.
