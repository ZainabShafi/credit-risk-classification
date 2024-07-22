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

The stages of the ML process were as follows: 

1) Splitting data into training/testing data sets
   a) Class balance visualization
   b) Creating y(target) and X(features) variables from isolated data
   c) Splitting into train and test, selecting 30% of the data as test data

2) Creating and predicting using the LogisticRegression model:
   a) Fitting the model using LogisticRegression func and save in var ("lending_model")
   b) Saving testing data labels predictions in var ("lend_test_predict")
   c) Populating confusion matrix and classification report

## Results



## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
