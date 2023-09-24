# credit-risk-classification

## Overview of the Analysis

In this analysis, we aim to address the challenge of credit risk classification, a problem inherently imbalanced because healthy loans outnumber risky loans. To tackle this issue, we employ various techniques to train and evaluate machine learning models. Our dataset comprises historical lending activity from a peer-to-peer lending services company, and our goal is to build a model that can effectively identify the creditworthiness of borrowers.

The analysis is structured as follows:

1. **Data Preparation**:
   - We split the data into training and testing sets.
   - Create a Logistic Regression Model with the Original Data.
   - Predict a Logistic Regression Model with Resampled Training Data.

2. **Model Evaluation and Comparison**:
   - We evaluate the performance of both the original and resampled data models.
   - Assess their ability to predict both healthy (0) and high-risk (1) loans.

3. **Credit Risk Analysis Report**:
   - We summarize and analyze the results from both machine learning models.
   - Compare the predictions made on the original and resampled datasets.
   - Provide recommendations based on model performance.

## Results

### Logistic Regression Model with Original Data
- Balanced Accuracy Score: [Balanced accuracy score for the original data model]
- Precision Score for High-Risk Loans (Label 1): [Precision score for label 1]
- Recall Score for High-Risk Loans (Label 1): [Recall score for label 1]

                   pre       rec       spe        f1       geo       iba       sup

          0       1.00      1.00      0.90      1.00      0.95      0.90     18781
          1       0.86      0.90      1.00      0.88      0.95      0.89       603

avg / total       0.99      0.99      0.90      0.99      0.95      0.90     19384

### Logistic Regression Model with Resampled Data
- Balanced Accuracy Score: [Balanced accuracy score for the resampled data model]
- Precision Score for High-Risk Loans (Label 1): [Precision score for label 1]
- Recall Score for High-Risk Loans (Label 1): [Recall score for label 1]

                   pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      1.00      1.00      1.00      0.99     18781
          1       0.86      1.00      0.99      0.92      1.00      0.99       603

avg / total       1.00      0.99      1.00      1.00      1.00      0.99     19384

## Summary

Both machine learning models were evaluated to predict credit risk, with one using the original dataset and the other employing resampled data with equal representation of healthy and high-risk loans. Here's a summary of the results and recommendations:

- The original data model achieved [balanced accuracy score = 0.9464452283780631] with [precision score = 86%] and [recall score = 90% ] for high-risk loans.

- The resampled data model achieved [balanced accuracy score = 0.9957592281038412] with [precision score = 86%] and [recall score = 100%] for high-risk loans.

In summary, while both models showed similar balanced accuracy scores, the resampled data model demonstrated better precision and recall for high-risk loans. This suggests that the oversampled model is more effective at identifying and correctly classifying high-risk loans, a critical task in credit risk assessment.

Recommendation:
- Based on the performance metrics, the logistic regression model trained with resampled data using RandomOverSampler is recommended for predicting credit risk. This model provides better precision and recall for high-risk loans.
- However, the choice of model should consider specific business requirements and goals. Further fine-tuning may be necessary to balance precision and recall, depending on the cost associated with false positives and false negatives.