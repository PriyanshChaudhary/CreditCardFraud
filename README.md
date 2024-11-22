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

### Benchmarking with LR Model
Train Accuracy: 0.9734843470048808
Test Accuracy: 0.9815846050822965
Train Recall: 0.9656887406112921
Test Recall: 0.8842105263157894

### Setting Benchmark as:
Recall : 88%
precision : 8%
f1=Score : 14%




