# Bank Marketing Outcome
Binary Supervised Learning Problem with Structured Data


## Description
This dataset is used to predict whether a client will subscribe to a term deposit at a bank, making it a binary classification problem.

## Features 
Includes client demographics (age, job, marital status), economic indicators, and previous marketing campaign outcomes.

## Source
Available on the UCI Machine Learning Repository (Bank Marketing Dataset).


# Explore Dataset.ipynb
Fast Check Up of the Data and Benchmarking

Steps:
* Simple Cleanup and One-Hot-Encoding of Variables
* Correlation and drop unimportant(and high correlated) columns
* Simple Logistic Regression
* Simple LazyPredict

## Model Benchmarking - bank.csv (4521, 44)

| ipynb               | package   | model              | norm | balance | rocauc | f1-score | f1-minor |
|---------------------|-----------|--------------------|------|---------|--------|----------|----------|
| Explore Dataset.ipynb | scikit-learn | Logistic Regression | Yes  | Yes      | 0.84   | 0.90     | 0.52     |
| Explore Dataset.ipynb | scikit-learn | Logistic Regression | Yes  | No      | 0.63   | 0.90     | 0.38     |
| Explore Dataset.ipynb | scikit-learn | Logistic Regression | No  | No      | 0.60   | 0.89     | 0.32     |
| Explore Dataset.ipynb | LazyPredict  | NearestCentroid       | Yes   | No     | 0.74   | 0.86     | 0.38     |
| Explore Dataset.ipynb | LazyPredict  | NearestCentroid       | No   | No     | 0.77   | 0.85     | 0.32     |

