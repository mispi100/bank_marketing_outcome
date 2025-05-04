# Bank Marketing Outcome
Binary Supervised Learning Problem with Structured Data

# Goal
Try different libraries and implement (deep) neural networks.

# ToDo
* Test Pytorch, Keras
* Use whole dataset
* Auswertung/Annäherung Feature Importance Neuronales Netz
* Cross-Validation - Overfitting

## Description
This dataset is used to predict whether a client will subscribe to a term deposit at a bank, making it a binary classification problem.

## Features 
Includes client demographics (age, job, marital status), economic indicators, and previous marketing campaign outcomes.

## Source
Available on the UCI Machine Learning Repository (Bank Marketing Dataset).


# Explore Dataset.ipynb
Fast Check Up of the Data and Benchmarking

# Manual Single-Neuron Model.ipynb
Implementation of Single-Layer Neural Network

# Manual Single-Layer Neural Network.ipynb
Implementation of a Neural Network with one Hidden Layer

# Manual L-Layer Neural Network.ipynb
Implementation of a Neural Network with L-Layer

Steps:
* Simple Cleanup and One-Hot-Encoding of Variables
* Correlation and drop unimportant(and high correlated) columns
* Simple Logistic Regression
* Simple LazyPredict
* Build Neural Networks with Numpy


## Model Benchmarking - bank.csv (4521, 44) 10% of Full Data

| ipynb               | package   | model              | norm | balance | rocauc | f1-score | f1-minor |
|---------------------|-----------|--------------------|------|---------|--------|----------|----------|
| Explore Dataset.ipynb | scikit-learn | Logistic Regression | Yes  | Yes      | 0.84   | 0.90     | 0.52     |
| Explore Dataset.ipynb | scikit-learn | Logistic Regression | Yes  | No      | 0.63   | 0.90     | 0.38     |
| Explore Dataset.ipynb | scikit-learn | Logistic Regression | No  | No      | 0.60   | 0.89     | 0.32     |
| Explore Dataset.ipynb | LazyPredict  | NearestCentroid       | Yes   | No     | 0.74   | 0.86     | 0.38     |
| Explore Dataset.ipynb | LazyPredict  | NearestCentroid       | No   | No     | 0.77   | 0.85     | 0.32     |
| Explore Dataset.ipynb | tpot  | TPOTClassifier       | Yes   | No     | 0.77   | 0.85     | 0.32     |
| Manual Single-Neuron Model.ipynb | numpy | Single-Neuron Model | No | No | 0.52 | 0.84 | 0.12 |
| Manual Single-Neuron Model.ipynb | numpy | Single-Neuron Model | Yes | No | 0.83 | 0.83 | 0.47 |
| Manual Single-Layer Neural Network.ipynb | numpy | 26Neuron Model | Yes | Yes | 0.72 | 0.80 | 0.49 |
| Manual L-Layer Neural Network.ipynb | numpy | (20,6,1) | Yes | No | 0.67 | 0.87 | 0.41 |
| Manual L-Layer Neural Network.ipynb | numpy | (20,6,1) | Yes | Yes | 0.75 | 0.89 | 0.52 |


