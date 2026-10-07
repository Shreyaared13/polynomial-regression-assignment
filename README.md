# Polynomial Regression Assignment (MS2026012)

## Overview

This repository contains my solution for Assignment 1: Polynomial Regression.

The objective is to predict the target variable **y** for two independent datasets using **Polynomial Regression** models only.

The degree of the polynomial was selected through systematic experimentation using cross-validation and evaluation metrics such as:

- Mean Squared Error (MSE)
- R² Score (Coefficient of Determination)

---

## Dataset Description

### Problem 1: Power Plant Steam Turbine Optimisation (var1)

- Input Features: x1, x2, x3, x4, x5, x6
- Target Variable: y
- Maximum polynomial degree allowed: 10

### Problem 2: Subterranean Thermal Reservoir Mapping (var2)

- Input Features: x1, x2, x3
- Target Variable: y
- Maximum polynomial degree allowed: 20

---

## Methodology

### Model Selection

For each dataset:

1. Generated polynomial features for multiple degrees.
2. Trained a Linear Regression model on the transformed features.
3. Evaluated performance using:
   - Training MSE
   - Cross-Validation MSE
   - Training R²
   - Cross-Validation R²
4. Selected the optimal degree based on the lowest cross-validation error.
5. Performed additional feature subset experiments to analyse the contribution of input variables.
6. Retrained the chosen model on the full training dataset.
7. Generated predictions for the test dataset.

---

## Final Models

### var1

- Features Used: x1, x2, x3, x4, x5, x6
- Selected Polynomial Degree: **<replace_with_best_degree>**

### var2

- Features Used: x1, x2, x3
- Selected Polynomial Degree: **<replace_with_best_degree>**

---

## Analysis Performed

The notebook includes:

- Degree vs MSE plots
- Degree vs R² plots
- Feature Subset vs R² plots
- Cross-validation performance tables
- Final prediction generation

These analyses were used to identify the best-performing polynomial degree while avoiding underfitting and overfitting.

---

## Repository Structure

```text
.
├── Polynomial_Regression.ipynb
├── MS2026012_train_var1.csv
├── MS2026012_test_var1.csv
├── MS2026012_train_var2.csv
├── MS2026012_test_var2.csv
├── MS2026012_pred_var1.csv
├── MS2026012_pred_var2.csv
└── README.md
```

---

## Files

### Notebook

- `Polynomial_Regression.ipynb`
  - Degree search
  - Cross-validation analysis
  - Feature subset analysis
  - Training and prediction pipeline

### Prediction Files

- `MS2026012_pred_var1.csv`
- `MS2026012_pred_var2.csv`

---

## Requirements

Install the required libraries:

```bash
pip install pandas numpy matplotlib scikit-learn
```

---

## How to Run

1. Clone the repository.

```bash
git clone <repository_link>
```

2. Open the notebook:

```bash
Polynomial_Regression.ipynb
```

3. Execute all cells.

4. Prediction files will be generated automatically:

```text
MS2026012_pred_var1.csv
MS2026012_pred_var2.csv
```

---

## Evaluation Metrics

The models were evaluated using:

### Mean Squared Error (MSE)

Measures the average squared prediction error.

### R² Score

Measures how well the model explains the variance in the target variable.

---

## Author

Shreya Konatham

MS2026012
