Customer Churn Prediction using Machine Learning
================================================

Customer retention is a critical objective for many businesses, as retaining existing customers is often more cost-effective than acquiring new ones. Customer churn is influenced by multiple factors, including service quality, usage behavior, support experience, and payment patterns. Understanding these factors enables organizations to identify customers at risk of leaving and take proactive actions to improve retention.

This project focuses on classifying customers as churned or non-churned based on a range of behavioral, contractual, and demographic features. The dataset includes information such as customer tenure, usage frequency, support interactions, payment delays, subscription type, and contract length.

The workflow involves preprocessing the dataset, training, and comparing multiple machine learning classifiers to identify models capable of accurately predicting customer churn while maintaining strong generalization performance.

📄 **Final report:** [report.pdf](https://github.com/MohammadAtabaki/Customer-Churn-Classification/blob/main/report.pdf)

* * * * *

📌 Project Overview
-------------------

Customer churn prediction is a key task in customer analytics, enabling organizations to identify customers at risk of leaving and take proactive retention actions.

In this project:

-   Exploratory Data Analysis (EDA) is performed to understand customer behavior.

-   Multiple machine learning models are implemented and optimized.

-   Model performance is evaluated and compared using standard classification metrics.

* * * * *

🧠 Models Implemented
---------------------

The following models were trained and evaluated:

-   **Random Forest**

-   **XGBoost**

-   **LightGBM**

Each model was tuned using **Randomized Search with cross-validation** to ensure strong generalization and avoid overfitting.

* * * * *

⚙️ Methodology
--------------

### Data Preprocessing

-   Removal of invalid and empty rows

-   Handling of categorical variables using encoding

-   Feature scaling where appropriate

-   Verification of label distribution (no severe class imbalance)

### Model Training & Tuning

-   Hyperparameter optimization via **RandomizedSearchCV**

-   5-fold cross-validation for robust parameter selection

-   ROC-AUC used as the primary optimization metric for churn prediction

### Evaluation

Models were evaluated on a held-out test set using:

-   Accuracy

-   Precision

-   Recall

-   F1-score

-   ROC-AUC

Overfitting was assessed by comparing training and test performance.

* * * * *

📊 Results Summary
------------------

All models achieved **near-perfect performance**, indicating strong predictive capability and excellent generalization.

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
| --- | --- | --- | --- | --- | --- |
| Random Forest | 0.99976 | 0.99996 | 0.99962 | 0.99979 | 1.00000 |
| XGBoost | 0.99985 | 1.00000 | 0.99974 | 0.99987 | 0.99999 |
| LightGBM | 0.99983 | 0.99996 | 0.99974 | 0.99985 | 1.00000 |

Since performance differences are marginal, model selection can be guided by **efficiency and deployment considerations** rather than accuracy alone.
