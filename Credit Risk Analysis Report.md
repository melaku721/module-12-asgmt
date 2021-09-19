Credit Risk Analysis Report
===

This analysis report will explain how the model identify the credit worthiness of the borrowers.

By using a dataset of historical lending activity from a peer-to-peer lending services company as the original dataset and predict a logistic regression model with oversampled trining data.

From the original dataset by assigning the "loan status" for "y" value and the "y" value counted and classified as "0" and "1". "0" is for "Healthy Loans" and "1" is for High-Risk Loan.

Applied a logistic Regration by using the imbalanced-learn library to compare the two virsion of the  datasets:- the original dataset and the resampled data.For both cases the target classes get counted,  train logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix and generate a classification report. 

## As a result when we compare the two models
* Model 1: with the original dataset
  * The accuracy score is high at 0.956677 or around 96%.
  * The precission is very high for the Healthy Loan which is "0" class(0.97) and very low for High-Risk Loan which is "1" class(0.04)
  * The recall for the "0" class is very high (0.97) and very low for the "1"class (0.04)
* Model 2: using the resampled data
  * The accuracy score is very higher at 0.99702 or around 100%.
  * The precission is very high for the Healthy Loan which is "0" class(1.00) and lower for High-Risk Loan which is "1" class(0.84)
  * The recall for the Healthy Loan and High-Risk Loan, ("0" and "1")classes almost matches(0.99 and 1.00)

## Summary
As we have seen above the accurecy score for the model with oversamled data is higher and the precition for the "1" class(High_Risk loan) with oversampled data is much higher. And also the recall for the "1" class with the oversampled data is much higher. so that the model that used the oversample data is more accurate at predicting the healthy loan and the risky loan.

As there is a credit risk classification because of the healthy loans easily outnumbered risky loans, the model used oversampling is balances and fix this problem. But while fixing this problem the model we used may increase the number of risky loans. This means we will have a high number of high-risk loan while identifying the credit worthiness of the borrowers. As a conclusion using oversampling for this model is not recommended.  

