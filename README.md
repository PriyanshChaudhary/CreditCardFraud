# CreditCardFraud
Develop a machine learning model to detect fraudulent transactions using a Kaggle dataset, focusing on data handling, model training, evaluation, and explainability. 

# Data Volume:

(283726, 31)

# Class	proportion:

0    	99.83%

1    	0.17%

### Observation
- No nulls found in data
- Data is highly imbalance with 0.1% minority class

# Feature Analysis

## Time & amount were the only interpretable features:
- Observed that less consecutive time has more fraud probability
- Hence, creating new flag features for additional uplift
