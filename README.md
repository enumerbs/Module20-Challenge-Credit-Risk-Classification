# Module20-Challenge-Credit-Risk-Classification

Data Analytics Boot Camp - Module 20 - Credit Risk Classification \
Supervised Learning Challenge

---

# 'Credit Risk' Analysis Report

## Overview of the Analysis

 This analysis reviewed a dataset of historical lending activity, in order to build a 'Credit Risk' model that can identify the creditworthiness of borrowers.

 The dataset consisted of a mix of loans determined to be either "Healthy" or "High-risk":
 - Healthy loan: 75,036 (96.8%)
 - High-risk loan: 2,500 (3.2%)

A number of different approaches to the classification modelling were used, and the model results are summarised below, along with a recommendation on the best model. In each case, the output of the model is a classification of each loan as either "Healthy" or "High-risk", according to the loan and borrower-related information given to the model - namely, the following aspects:
- loan size (amount)
- interest rate
- borrower income
- debt-to-income ratio
- borrower's number of accounts, and
- derogatory remarks.

Each of the classification models used those aspects to predict whether each loan should be classifed as "Healthy" or "High-risk", and the predictions were compared against the known results of the original dataset. Specifically, each classification models was trained on 75% of the original dataset, with the remaining 25% of the original dataset being used for model evaluation and comparison.

## Analysis Results

1. Logistic Regression Model (Original Data):
    - 99% Accuracy overall
    - 87% Precision for High-risk loans
    - 95% Recall for High-risk loans
    - 91% f1-score for High-risk loans

1. Decision Tree Model: (Original Data)
    -  99% Accuracy overall
    -  87% Precision for High-risk loans
    -  80% Recall for High-risk loans
    -  83% f1-score for High-risk loans

1. Logistic Regression Model (Scaled Original Data):
    -  99% Accuracy overall
    -  87% Precision for High-risk loans
    -  98% Recall for High-risk loans
    -  92% f1-score for High-risk loans

1. SVC Model (Scaled Original Data):
    -  99% Accuracy overall
    -  87% Precision for High-risk loans
    -  98% Recall for High-risk loans
    -  92% f1-score for High-risk loans


## Results Summary & Model Recommendation

Recommended model: **Linear Support Vector Classifier (SVC)**

The SVC model performed the best, as it was as accurate as the other models but performed better (lower numbers) for false-negative and false-positive classifications.

The Logistic Regression Model based on the Scaled Data (that is, the original data set with standard scaling applied) performed almost as well as the SVC model, so that could be considered an alternative model.

 The rationale for this choice is that, in terms of our 'Credit Risk' scenario, it's more important we have a low false-negative rate (that is, we would prefer to minimise the number of times we predict a loan to be Healthy when it is, in fact, High-risk).

# References

The following references were used in the development of the solution for this Challenge.

## Feature Scaling
- Article: "Which Machine Learning requires Feature Scaling (Standardization and Normalization) and which not?" https://www.kaggle.com/discussions/getting-started/159643


## Supervised Learning
- Class notes/student activity files for 'Supervised Learning', Monash University 'Data Analytics Boot Camp', including Jupyter Notebooks, were used as references and implementation guides.