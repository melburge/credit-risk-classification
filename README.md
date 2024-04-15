Module 20 Report


Credit Risk Analysis Report - M Burge.


        Credit Risk Analysis Objective:

The objective of this analysis is to construct a supervised machine learning model capable of discerning between safe and risky loans based on borrower and loan characteristics. With a dataset comprising 77,537 loan entries, encompassing various financial attributes of borrowers and loans, the challenge lies in effectively training the model to accurately classify the relatively small fraction of loans labeled as risky, amounting to 2,500 entries or 3.22%.

        Methodology:

Data Preparation: The dataset underwent preprocessing to segregate the loan status as 'healthy' or 'risky' as the target variable, while the remaining attributes were designated as features for model training.
y variable = Label (Loan Status column).
X variable = Features (all other columns in the dataset).

Data Segmentation: To facilitate model training and validation, the dataset was divided into distinct training and testing subsets using sklearn and aplying a random state of 1.
X_train, X_test, y_train, y_test = train_test_split(X, y, random_state = 1)

Model Development: Employing the Logistic Regression algorithm from the sklearn library, with the Limited-memory 'lbfgs' solver, the model was constructed. Logistic Regression was chosen due to its suitability for binary classification tasks and accuracy with financial data.

Model Training: The Logistic Regression model was trained on the training dataset to discern underlying patterns and relationships indicative of loan health or risk.

Prediction and Evaluation: Subsequently, predictions were generated using the test dataset, enabling an assessment of the model's predictive performance by comparing these predictions with the actual loan classifications.

        Performance Evaluation:

Overall Accuracy: 99%
Balanced Accuracy: 97%

        Precision:
Healthy Loans: Precision score of 100%
Risky Loans:   Precision score of 84%.

        Recall:
Healthy Loans: Recall score of 99%.
Risky Loans:   Recall score of 94%.


RESULTS

Accuracy Scores:

Description of Model 1 Accuracy, Precision, and Recall scores.

    Accuracy:          0.99
    Balanced Accuracy: 0.97
    
    Precision
    Healthy:           1.00
    High-Risk:         0.84
    
    Recall
    Healthy:           0.99
    High-Risk:         0.94
    
    
      Report:
                  precision    recall  f1-score   support

           0           1.00      0.99      1.00     18765
           1           0.84      0.94      0.89       619

    accuracy                               0.99     19384
    macro avg          0.92      0.97      0.94     19384
    weighted avg       0.99      0.99      0.99     19384




SUMMARY

Strengths and Limitations

Strengths:
Excellent precision in predicting healthy loans.
Adequate data points available for training healthy loan classification.

Limitations:
Insufficient representation of high-risk loan data.
Limited loan value range (up to $23,500).
Suboptimal performance in accurately identifying high-risk loans.

Recommendations:
While the model may suffice for scenarios involving loans below $23,500 and historical loan distribution aligning with the dataset proportions, caution is advised for broader applications or instances necessitating nuanced risk assessment. Supplementary risk evaluation mechanisms and contextual considerations beyond the model's predictions should be incorporated into lending decision-making processes to mitigate potential risks effectively. 

Key Findings:
While the Logistic Regression model exhibits exceptional precision in identifying healthy loans, it shows a notable limitation in accurately classifying risky loans, with approximately 10% being misclassified as healthy. This discrepancy raises concerns, particularly regarding the potential financial ramifications associated with defaults on high-risk loans. Furthermore, the scarcity of high-risk loan data poses a challenge to the model's learning process, potentially impeding its ability to generalise effectively.
