# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithm).



Credit Risk Analysis Overview:

The objective of this analysis is to construct a supervised machine learning model capable of discerning between safe and risky loans based on borrower and loan characteristics. With a dataset comprising 77,537 loan entries, encompassing various financial attributes of borrowers and loans, the challenge lies in effectively training the model to accurately classify the relatively small fraction of loans labeled as risky, amounting to 2,500 entries.

Our Methodology:

Data Preparation: The dataset underwent preprocessing to segregate the loan status (healthy or risky) as the target variable, while the remaining attributes were designated as features for model training.

Data Segmentation: To facilitate model training and validation, the dataset was divided into distinct training and testing subsets.

Model Development: Employing the Logistic Regression algorithm from the sklearn library, with the Limited-memory BFGS ('lbfgs') solver, the model was constructed. Logistic Regression was chosen due to its suitability for binary classification tasks.

Model Training: The Logistic Regression model was trained on the training dataset to discern underlying patterns and relationships indicative of loan health or risk.

Prediction and Evaluation: Subsequently, predictions were generated using the test dataset, enabling an assessment of the model's predictive performance by comparing these predictions with the actual loan classifications.

Performance Evaluation:

Overall Accuracy: Achieved a commendable accuracy of 99.185%.
Balanced Accuracy: Demonstrated a balanced accuracy score of 95.205%.
Precision:
Healthy Loans: Precision score of 100%.
Risky Loans: Precision score of 85%.
Recall:
Healthy Loans: Recall score of 99%.
Risky Loans: Recall score of 91%.
Key Findings:

While the Logistic Regression model exhibits exceptional precision in identifying healthy loans, it shows a notable limitation in accurately classifying risky loans, with approximately 10% being misclassified as healthy. This discrepancy raises concerns, particularly regarding the potential financial ramifications associated with defaults on high-risk loans. Furthermore, the scarcity of high-risk loan data poses a challenge to the model's learning process, potentially impeding its ability to generalize effectively.

Strengths and Limitations:

Strengths:

Excellent precision in predicting healthy loans.
Adequate data points available for training healthy loan classification.
Limitations:

Insufficient representation of high-risk loan data.
Limited loan value range (up to $23,500).
Suboptimal performance in accurately identifying high-risk loans.

Recommendations:

While the model may suffice for scenarios involving loans below $24,000 and historical loan distribution aligning with the dataset proportions, caution is advised for broader applications or instances necessitating nuanced risk assessment. Supplementary risk evaluation mechanisms and contextual considerations beyond the model's predictions should be incorporated into lending decision-making processes to mitigate potential risks effectively.
## Results

Accuracy Scores:

Machine Learning Model 1:
Description of Model 1 Accuracy, Precision, and Recall scores.
    Accuracy: 0.99
    Balanced Accuracy: 0.97
Precision
    Healthy:           1.00
    High-Risk:         0.84
Recall
    Healthy:           0.99
    High-Risk:         0.94
    
              precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.94      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384




## Summary
Strengths and Limitations:

Strengths:

Excellent precision in predicting healthy loans.
Adequate data points available for training healthy loan classification.
Limitations:

Insufficient representation of high-risk loan data.
Limited loan value range (up to $23,500).
Suboptimal performance in accurately identifying high-risk loans.

Recommendations:

While the model may suffice for scenarios involving loans below $23,500 and historical loan distribution aligning with the dataset proportions, caution is advised for broader applications or instances necessitating nuanced risk assessment. Supplementary risk evaluation mechanisms and contextual considerations beyond the model's predictions should be incorporated into lending decision-making processes to mitigate potential risks effectively.

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
