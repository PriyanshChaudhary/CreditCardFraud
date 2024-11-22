# CreditCardFraud
Develop a machine learning model to detect fraudulent transactions using a Kaggle dataset, focusing on data handling, model training, evaluation, and explainability. 

# Data Volume:

(283726, 31)

# Class	proportion:

0  => 99.83%

1  => 0.17%

### Observation
- No nulls found in data
- Data is highly imbalance with 0.1% minority class

# Feature Analysis

## Time & amount were the only interpretable features:
- Observed that less consecutive time has more fraud probability
- Hence, creating new flag features for additional uplift


## Handling Imbalanced Data
- Instead of accuracy, use recall precision for accurate analysis of Fraud Class
- Using Stratified Splitting to ensure that the proportion of each class during the split remains correct.

### Using SMOTE¶
to balance the class distribution

# Model Building :  Supervised

### Benchmarking with LR Model
- Train Accuracy: 0.9734843470048808
- Test Accuracy: 0.9815846050822965
- Train Recall: 0.9656887406112921
- Test Recall: 0.8842105263157894

## Setting Benchmark as:
- Recall : 88%
- precision : 8%
- f1-Score : 14%

### Xgboost Modelling

## Update Metrics with XGB:

#### Accuracy
- Train Accuracy: 1.0
- Test Accuracy: 0.99
- Cross-Validation Accuracy: 0.99

#### Precision
- Train Precision: 1.0
- Test Precision: 0.82

#### Recall
- Train Recall: 1.0
- Test Recall: 0.8

## Model Observations
- As XGBoost has more AUC then LGM, it is a better model.
- the XGBoost metrics significantly surpassed the Benchmark Scores
- the Scores below indicate thet while benchmark model has higher recall, it gave significantly more False Positives.
- The XBG was able to maintain the recall while increase Precision by 10X

## Current XGBoost performance is:
- Recall : 80%
- precision : 82%
- f1Score : 81%


