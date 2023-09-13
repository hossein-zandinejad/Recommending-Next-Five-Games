# Recommending Next Five Games
CafeBazaar Summer School 2021 Project

![CafeBazaar Logo](cafebazaarlogo_1.png)

## Table of Contents
- [Abstract](#abstract)
- [Introduction](#introduction)
- [The Dataset and Features](#the-dataset-and-features)
- [Methods](#methods)
  - [I. Random Forest](#i-random-forest)
  - [II. Logistic Regression](#ii-logistic-regression)
  - [III. SVM](#iii-svm)
- [Future Works](#future-works)
- [Installation](#installation)
- [Conclusion](#conclusion)
- [References](#references)

## Abstract
This repository explores the development of a recommender system aimed at predicting the next five games a user might install based on their previous choices. The project leverages techniques from classification and machine learning to achieve this goal.

## Introduction
The primary objective of this project is to recommend the next set of games a user might be interested in, based on their historical choices. This capability is widely used in various applications, including App Stores, Video Streaming Websites, and Online Shops.

The project begins by describing the dataset and data preprocessing techniques. It then explores the feasibility of addressing the recommendation task using classification techniques. Multiple machine learning models are employed, and the most accurate model is selected.

One of the key challenges faced during the project is related to the CSR Matrix, where the number of features varies per training example. Various strategies, including feature reduction methods, are employed to address this issue.

## The Dataset and Features
The dataset used for this project is the SummerCamp 1400 CafeBazaar dataset. It consists of three features: "id," "historical games," and "next game." The "id" feature is the user ID, which is not crucial for this project and is excluded. The "historical games" feature represents the user's previously installed games as a string of game IDs. The "next game" feature is an integer representing the ID of the next game the user will install.

The game IDs range from 1 to 7489, but the majority of "next game" IDs fall between 1 and 600, potentially leading to overfitting. Feature transformation using a CSR Matrix results in a dataset with 7736 features.

## Methods
### I. Random Forest
Random Forest, a classification ensemble method, is employed to predict user preferences. It uses decision trees constructed on bootstrapped observations and decorrelates the trees by examining a random sample of features. A Random Forest model with specific parameters achieved an accuracy of 15.2%.

### II. Logistic Regression
L2-norm Logistic Regression is used as the baseline discriminative model. It minimizes a cost function that balances model fitting and overfitting penalties. This model achieved an accuracy of 16.7% with specific hyperparameters.

### III. SVM
Support Vector Machine (SVM) is another model used in this project, which minimizes a cost function subject to certain constraints. Python's sklearn package is utilized for implementation.

## Future Works
Given more time, several potential improvements and explorations can be considered. These include experimenting with XGBoost models, fine-tuning Random Forest models with different parameters, and exploring ensemble methods to combine classifiers. Additionally, Bayesian Model Averaging (BMA) could be investigated as a potential ensemble method.

## Installation
To run this project, you need to install the following libraries and dependencies:

```bash
pip install numpy pandas scikit-learn scipy
```
## Conclusion
This project embarked on the development of a recommender system for predicting a user's next five game choices. Exploratory Data Analysis (EDA), feature engineering using a sparse matrix, and the application of various machine learning models were undertaken. Among these models, Logistic Regression demonstrated the best performance in predicting the next five games.

## References
- Kim Falk. "Practical Recommender Systems." Manning, 2019.
- Baptiste Rocca. "Introduction to recommender systems," 2019.
- Aditya Sharma. "Beginner tutorial: Recommender systems in python," 2019.
- Sklearn. "Logisticregression."
- Sklearn. "Random Forrest."
