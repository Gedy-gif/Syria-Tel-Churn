# Customer-Churn-Analysis
### Overview

Customer churn (also called attrition) refers to the number of subscribers who discontinue services within a given time period.
It is a critical threat to growth, even with strong new customer acquisition. For telecom companies, where competition is fierce and switching costs are low, reducing attrition is essential to protect profitability.
Predicting churn enables proactive retention strategies, such as targeted discounts or improved services.

### Objectives

- Identify the current churn rate.
- Identify What patterns precede churn.
- Identify the best retention strategies..
- Identify which service erodes more revenue to Churn.

### Data source

The dataset used for this project is from Kaggle: [Churn in Telecoms Dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)

### Key Features

* Dataset: ~33,300 rows with features like state, account length, area code, phone no., total minutes used per call, customer service, churn e.t.c.
* Preprocessing: SMOTE for class imbalance, encoding for categorical variables, outlier handling.
* Model: Random Forest Classifier (best_rf) .
* Evaluation: Precision, recall, F1 score, ROC AUC; visualizations include Feature Importance Plot, Confusion Matrix (implied), and recommended Precision-Recall, SHAP, ROC curves.

### Key Insights

- Top predictors: Duplication, data structure, consistency, distribution check, unique values check.
- SMOTE improves default detection.
- Feature Importance Plot clarifies key factors; SHAP (recommended) enhances fairness analysis.
- Confusion Matrix (implied) supports reliable automation.
- ROC Curve (drafted) shows Random Forest outperforms Logistic Regression.

### Setup

- Clone the repository.
- Install dependencies: pip install -r requirements.txt.
- Run index.ipynb in Jupyter Notebook.

## Exploratory Data Analysis (EDA) 
- Churn Rate
- Churn vs Revenue
- Factors that contribute most to customer churn.
- Usage pattern Analysis
- Customer Service Analysis
- Geographic Analysis

[text](Images)


### Churn Distribution
- From the class distribution, we observe that 85.5% of the customers did not churn while only 14.5% churned. This shows a significant class imbalance.

### Factors that contribute most customers to churn.
+ To better understand what drives customers to leave, I grouped the variables into thematic areas and explored their impact on churn. These factors include:
   - Account Length - to understand if longer-term customers are more or less likely to churn.
   - Geographical Factors - to detect regional or location-based trends in churn.
   - International Plan & Voice Mail Plan — Does having specific plans influences churn likelihood
   - Usage Behavior — Does high or low usage patterns are linked to churn.
   - Financial Impact (Charges): to evaluate if higher billing is associated with customer dissatisfaction and churn.
   - Number of Customer Service Calls — Does frequent service contact signals dissatisfaction.

### Requirements

- Python 3.x
- Libraries: pandas, numpy, scikit-learn, imblearn, matplotlib, seaborn, shap, lime.

### Usage

- Load data and preprocess in index.ipynb.
- Train model and evaluate using provided metrics and plots.
- Ordinal encoding.

## Modeling

- Objective
    - This helps the company proactively retain customers likely to stop using the service. The goal is to predict customer churn for SyriaTel using available customer data. 

### Models Used
- Basic logistic Regression.
- Regularized logistic Regression.
- Smote
- Random Forest.

Advanced Random Forest
+ Proven Performance
- Recall (77%): Captures 77 out of 100 at-risk customers while being more realistic than the original 91% claim.
- Precision (81%): Identifies true churners with 19% false positives, balancing accuracy and operational costs.
- ROC AUC (0.931): Maintains excellent risk-ranking capability (94% accuracy), though slightly below the original 0.99 claim.


 ### Recomendations:
   - Run localized campaigns in high-churn states (Washington, Texas) with deeper nvestigation into region specific issues like service quality, network coverage or billing concerns.
   - Develop onboarding programs for new customers and loyalty program for long term customers to reduce early drop-offs and late disengagement.
   - Proactively monitor customers with 3+ surpport calls and prioritize them for resolution. Train customer service team to resolve issues on the first contact to prevent frustration.
   - Reassess the value proposition of the international plan. This could involve improving call quality, reducing costs, or bundling with other perks to increase satisfaction.
   - Introduce spending caps or usage notifications for customers who pay more especially during daytime & International calls to help manage expectations and reduce bill shock as these users are more likely to churn.
   - Have a higher budget for areas with a high churn rate for marketing.
