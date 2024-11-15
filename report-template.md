# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

# Purpose of Analysis 

The goal of this analysis was to create a predictive model to identify high-risk loans. By accurately forecasting which loans are likely to default, lenders can make more informed decisions, better manage risk, and reduce potential financial losses. Specifically, the analysis focused on building a logistic regression model to classify loans as either healthy (0) or high-risk (1).

* Explain what financial information the data was on, and what you needed to predict.

# The dataset contained various financial features related to individual loans, including:

loan_size: The total amount of the loan.
interest_rate: The interest rate applied to the loan.
borrower_income: The income of the borrower.
debt_to_income: The borrower's debt-to-income ratio.
num_of_accounts: The total number of accounts held by the borrower.
derogatory_marks: The number of negative marks on the borrower's credit report.
total_debt: The borrower's total outstanding debt.
loan_status: The target variable, indicating whether the loan is healthy (0) or high-risk (1).

# Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
    The target variable, loan_status, is binary.

# Describe the stages of the machine learning process you went through as part of this analysis.
    
1) **Data Preparation**: Loaded the dataset, examined its structure, and separated the features (X) from the target variable (y).  

2) **Data Splitting**: Divided the data into training and testing sets to evaluate the model on unseen data.  

3) **Model Selection and Training**: Selected the logistic regression algorithm for its simplicity and interpretability, and trained the model on the training data.  

4) **Making Predictions**: Used the trained model to generate predictions on the test data.  

5) **Evaluation**: Assessed the model's performance using a confusion matrix and classification report, evaluating precision, recall, and F1 score for both classes.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

- **Logistic Regression**: This algorithm was selected for its effectiveness in binary classification and its ability to deliver probabilistic outputs.  

- **Confusion Matrix and Classification Report**: These evaluation tools offered detailed insights into the model's performance, specifically across the two classes (healthy and high-risk loans).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

The logistic regression model was evaluated on its ability to predict loan statuses as either healthy (0) or high-risk (1), using performance metrics such as accuracy, precision, recall, and the F1 score, all derived from the confusion matrix and classification report.

**Which model performs best? How do you know it performs best?**  
The logistic regression model performs well, achieving high accuracy and solid metrics for both healthy and high-risk loans. Based on the evaluation results, it is clear that this model is effective for this classification task.

**Does performance depend on the problem we are trying to solve?**  
Yes, performance can depend on the specific problem at hand.

- **Class 0 (Healthy Loans):** Since healthy loans make up the majority class, high accuracy and precision for this class are important to minimize false positives—avoiding the misclassification of healthy loans as high-risk.
  
- **Class 1 (High-Risk Loans):** Accurately identifying high-risk loans is critical for reducing financial risk. A high recall score for this class (0.91) ensures that most high-risk loans are correctly flagged, which helps mitigate the risk of defaults.

**Business Objective:**  
If the primary goal is to minimize financial risk by identifying as many high-risk loans as possible, then recall for Class 1 becomes particularly important.

**Recommendation:**  
Given its high recall for Class 1 (0.91) and its balance between precision and recall, the logistic regression model is recommended. It effectively identifies high-risk loans while keeping false positives to a manageable level, making it a strong choice for minimizing financial risk.

## Final Recommendation:
Use the Logistic Regression Model: This model demonstrates strong performance across all key metrics, excelling at identifying high-risk loans—crucial for managing financial risk. Its high accuracy and balanced performance make it a dependable tool for predicting loan outcomes in this dataset.

By leveraging this model, lenders can more effectively manage their portfolios, make informed lending decisions, and minimize the risk of financial losses due to defaults.
