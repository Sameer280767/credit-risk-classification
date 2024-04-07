# credit-risk-classification

## Overview of the Analysis

* <u>Purpose of the analysis<u>

 - Using a dataset of historical lending activity from a peer-to-peer lending services company, build a model that can identify credit worthiness of customers

* <u>Data used and predictions made<u>

 - Historical data containing details of loans with a column detailing if the loan was healthy or risky was used

  - A model was built which would predict which loans were likely to be healthy or risky

* <u>Variables and model building<u>

 - Using Pandas a variable for the data as a dataframe was created

 - This data frame was split into a y variable as labels and X variable as features

 - This was further split into 2 datasets as training and testing datasets, with training dataset containing 75% of records

 - Above acton was done by  importing the train_test_split function from sklearn.model_selection module and splitting the data into training and testing sets with a random state of 1

 - This the data into training and testing sets, ensuring reproducibility of the split with a fixed random state

 - The LogisticRegression class from the sklearn.linear_model module in Python was used for logistic regression

 - Model was fitted to training data and predictions were made on the test data using LogisticRegression

*<u>Model performance<u>

 - Model prformance was judged by generating the confusion matrix and generating a classification report

 - Confusion matrix generated following 4 data points. 
 For health loans
  - TP: True positive. Loan was healthy and predicted healthy
  - FP: False positive.Loan was risky but predicted healthy
  - TN: True negative. Loan was risky and predicted risky
  - FN: False negative. Loan was healthy but predicted risky
For risky loans
  - TP: True positive. Loan was risky and predicted risky
  - FP: False positive.Loan was healthy but predicted risky
  - TN: True negative. Loan was healthy and predicted healthy
  - FN: False negative. Loan was risky but predicted healthy

Above numbers were used to calculate 

 - Precision - what % of predictions were correct. TP/(TP+FP)

 - Recall - what % of positive cases did the model catch. TP/(TP+FN)

 - f1 - what % of positive cases were correct

*<u>Summary of results:Predicting healthy loans<u>

 - Precision is high at almost 100%. False positive (predicted as healthy when they were risk) instances were 56. This led to a high precision score.

 - Recall too was high at 99.4%. False negatives (predicted as risky when healthy) intances were 102

 - To summarise model was very effcient in predicting healthy loans

*<u>Summary of results:Predicting risky loans<u>

 - Precision was at 85%. This was as Fasle Positives instances of molel predicting loan to be risky when they were healthy were 102

 - Recall wsa 91%. False negatives instances of model predicting loans as healthy when thy were risky were 56

 - To summarise model's recall % was high however not as good as for predicting healthy loans