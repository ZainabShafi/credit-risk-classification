# Module 12 Report Template


## Overview of the Analysis

The purpose of this analysis is to train and evaluate the performance of a supervised Machine Learning model based on loan risk. More specifically, it's ability to correctly predict labels for healthy loans (0) and unhealthy loans (0), further aiming to identify the credit-worthiness of borrowers. This analysis will utilize a dataset of historical lending activity from a peer-to-peer lending services company, which contains financial data related to loan applications - such as: 

loan_status: the status of approval of the loan.
loan_size: The amount of the loan requested by the borrower.
interest_rate: The interest rate assigned to the loan.
borrower_income: The annual income of the borrower.
debt_to_income: The ratio of the borrower's total debt to their income.
num_of_accounts: The number of credit accounts the borrower has.
derogatory_marks: The number of derogatory marks on the borrower’s credit report (e.g., late payments, collections, bankruptcies).
total_debt: The total amount of debt the borrower has.

This analysis utilizes "loan_status" as the target variable for the model to predict, and the remainder of the data as features to aid the model in its predictions/teaching. To evaluate the balance of classes for the "loan_status" data - this analysis utilized pandas function value_counts to plot a bar chart(Line 18, credit_risk_classifcation_ZS). This chart concluded that there is a major class imbalance, with most data points falling in the "0" or healthy loan class. 

The techonolgy usage and stages of the ML process were as follows: 

## Technologies Used

1. **Data Loading**: Utilizing `pandas` to load data from files.
2. **Data Splitting**: Using `train_test_split` from `scikit-learn` to divide the dataset into training and testing sets.
3. **Model Building**: Implementing logistic regression using `LogisticRegression` from `scikit-learn`.
4. **Model Evaluation**: Evaluating the model performance with `confusion_matrix` and `classification_report` from `scikit-learn`.

## Coding Logic 

A) Splitting data into training/testing data sets
   - Class balance visualization
   - Creating y(target) and X(features) variables from isolated data
   - Splitting into train and test, selecting 30% of the data as test data

B) Creating and predicting using the LogisticRegression model:
   -  Fitting the model using LogisticRegression func and save in var ("lending_model")
   - Saving testing data labels predictions in var ("lend_test_predict")
   - Populating confusion matrix and classification report

## Results

**Class 0 (healthy loan):**

Precision: 1.00
Recall: 0.99
F1-Score: 1.00
Support: 18,765

**Class 1 (high-risk loan):**

Precision: 0.85
Recall: 0.91
F1-Score: 0.88
Support: 619

**Overall Performance:**

Accuracy: 0.99

Macro Average:
Precision: 0.92
Recall: 0.95
F1-Score: 0.94

Weighted Average:
Precision: 0.99
Recall: 0.99
F1-Score: 0.99
Total Support: 19,384


## Summary

As exhibited by the results above, the model performs excellently in predicting healthy loan labels but needs improvement in predicting high-risk loans. The overall performance shows nearly perfect accuracy. However, due to the significant class imbalance, the model is trained predominantly on the majority class (healthy loans), leading to potential overfitting to this class.

Given the imbalanced nature of the data, the model struggles to predict high-risk loans with the same accuracy. This can lead to significant issues for stakeholders, as the model may not adequately identify weak loan applicants, resulting in unpreparedness for the risks associated with high-risk loans.

Therefore, I do not recommend using this model in its current form. It is crucial to address the class imbalance through techniques such as oversampling the minority class, undersampling the majority class, or using different algorithms (Random Forests for eg) that handle imbalance better to improve the model's ability to generalize across both classes.




