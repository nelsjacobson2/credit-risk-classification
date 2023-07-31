# Module 20 Report: Credit Risk Analysis using Logistic Regression

## Overview of the Analysis

The purpose of this analysis was to build machine learning models using logistic regression to predict credit risk for borrowers based on historical lending activity data. The dataset contained financial information on peer-to-peer lending, where a value of 0 in the "loan_status" column indicated a healthy loan, and a value of 1 indicated a high risk of defaulting.

The variables we aimed to predict were the loan_status labels, representing both healthy and high-risk loans. We initially observed the class distribution and found that the data was imbalanced, with significantly fewer instances of high-risk loans compared to healthy loans.

To address the class imbalance, we employed the RandomOverSampler from imbalanced-learn to resample the data, ensuring equal representation of both classes. The machine learning process included splitting the data into training and testing sets, fitting a logistic regression model with original data, and then repeating the process with the resampled data.

## Results

### Machine Learning Model 1: Logistic Regression (Original Data)

* Accuracy Score: 0.99
* Precision (Healthy Loans - Class 0): 1.00
* Recall (Healthy Loans - Class 0): 0.99
* F1-Score (Healthy Loans - Class 0): 1.00

* Precision (High-Risk Loans - Class 1): 0.85
* Recall (High-Risk Loans - Class 1): 0.99
* F1-Score (High-Risk Loans - Class 1): 0.92

### Machine Learning Model 2: Logistic Regression (Resampled Data)

* Accuracy Score: 0.99
* Precision (Healthy Loans - Class 0): 1.00
* Recall (Healthy Loans - Class 0): 0.99
* F1-Score (Healthy Loans - Class 0): 1.00

* Precision (High-Risk Loans - Class 1): 0.85
* Recall (High-Risk Loans - Class 1): 0.99
* F1-Score (High-Risk Loans - Class 1): 0.92

## Summary

Both machine learning models using logistic regression showed exceptional performance in predicting credit risk. The accuracy scores of 0.99 for both models indicate a high level of overall correctness in their predictions.

Model 1, which used the original data, demonstrated impressive precision, recall, and F1-scores for both healthy loans (class 0) and high-risk loans (class 1). The model effectively identified both healthy and high-risk loans, with a near-perfect precision and recall for class 0 and reasonably high values for class 1.

Model 2, with resampled data, achieved identical results to Model 1. The resampling process helped balance the class distribution, and the model excelled in identifying both types of loans, maintaining high precision and recall for both classes.

Recommendation: Based on the analysis, both models performed remarkably well in predicting credit risk. Since Model 2 utilized resampled data, which could provide more robust results on real-world imbalanced datasets, it is preferred for credit risk analysis. The model demonstrated a balanced precision-recall trade-off for both healthy and high-risk loans, making it reliable in identifying creditworthy borrowers and reducing the risk of misclassifying high-risk loans.

In conclusion, the logistic regression model trained with resampled data is recommended for use by the company for credit risk assessment, as it showcases exceptional performance in predicting both healthy and high-risk loans. The model's high accuracy, precision, and recall make it a valuable tool for making informed lending decisions and effectively managing credit risk.
