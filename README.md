# Credit Risk Classification

## Background

In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Instructions

The instructions for this Challenge are divided into the following subsections:

- Split the Data into Training and Testing Sets

- Create a Logistic Regression Model with the Original Data

- Predict a Logistic Regression Model with Resampled Training Data

- Write a Credit Risk Analysis Report

## Split the Data into Training and Testing Sets

Open the starter code notebook and use it to complete the following steps:

1. Read the ``` lending_data.csv ``` data from the Resources folder into a Pandas DataFrame.

2. Create the labels set ```(y)``` from the **“loan_status”** column, and then create the features ```(X)``` DataFrame from the remaining columns.

3. Split the data into training and testing datasets by using train_test_split.

## Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:

1. Fit a logistic regression model by using the training data (X_train and y_train).

2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

3. Evaluate the model’s performance by doing the following:

  - Calculate the accuracy score of the model.
  - Generate a confusion matrix.
  - Print the classification report.

4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

## Write a Credit Risk Analysis Report
### Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository.

- Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:

- **An overview of the analysis:** Explain the purpose of this analysis.

- **The results:** Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

- **A summary:** Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.


## Overview of the Analysis

Lending services company lend money to borrowers expecting them to complete the lending process after the contracted year terms. Credit risk is a measurement which lending companies used to determine whether the customer can afford the loan with many factors. This analysis will use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

- The report is to investigate the relationship between training imbalanced data and over sampling would have difference through logistic regression machine learning algorithm.

- Logistic regression is a supervised learning algorithm that is used to predict a categorical variable based on one or more predictor variables. The goal is to find the best set of coefficients that minimize the difference between the predicted attitude and the actual class labels.

#### Stages

![Screenshot 2023-03-22 222413](https://user-images.githubusercontent.com/116006523/227051928-e50be620-94f9-4234-810c-41eb29f34070.jpg)

- First of all, using ```value_counts``` to identify the balance of the target values which the dataset is highly imbalanced. 

![Screenshot 2023-03-22 222810](https://user-images.githubusercontent.com/116006523/227052636-9d11cd0f-b09b-4c3b-95be-bc4cdc74e8ec.jpg)

- Data splitted into training and testing datasets to fit into the logistic regression model. 

![Screenshot 2023-03-22 223102](https://user-images.githubusercontent.com/116006523/227053040-927671a7-ffb7-4ef5-83a4-63d13581e8b3.jpg)

- Confusion matrix is used to show how the model is performing on training. 

- Same methods are used for imbalanced dataset and oversampling dataset. 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

#### Machine Learning Model 1 (imbalanced dataset):
  ![Screenshot 2023-03-22 223632](https://user-images.githubusercontent.com/116006523/227054021-b78f8d84-e5b8-4d16-b7bc-39f198597c66.jpg)

![Screenshot 2023-03-22 223656](https://user-images.githubusercontent.com/116006523/227054032-ee4fe953-d601-4550-8235-1d91be7be1c4.jpg)

- For imbalanced data learning model, the accuracy score is 99.2%
- According to the models recall scores, the model made no mistakes when predicting healthy loans and made 11% of mistakes when predicted non-healthy loans.
- We are expecting a more precise training model but using oversampling method. 

#### Machine Learning Model 2 (Oversampling):
  ![Screenshot 2023-03-22 223721](https://user-images.githubusercontent.com/116006523/227054047-0b603481-dab3-4fe0-bc00-0977003d3fba.jpg)

![Screenshot 2023-03-22 223736](https://user-images.githubusercontent.com/116006523/227054067-f234ebd3-6306-48c7-afc4-27ea808234ff.jpg)

- For imbalanced data learning model, the accuracy score is 99.5%
- According to the models recall scores, the model made no mistakes when predicting healthy loans and non-healthy loans.

## Summary

###Model with imbalanced dataset:

*80 (FALSE POSITIVES) The predicted value is healthy but False

*67 (FALSE NEGATIVES) The predicted value is non-healthy but Positive


### Model with oversampled dataset:

*91 (FALSE POSITIVES) The predicted value is healthy but False

*2 (FALSE NEGATIVES) The predicted value is non-healthy but Positive

According to the confusion matrics, the number of FALSE NEGATIVES decreases from 67 to 2 which the model has improved in carrying out the predictions. Although the accuracy scores have no big difference, we intend to use the score with oversampled model as closer to 100% means the model is more accurate on predictions. 
