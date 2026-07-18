# Machine Learning-Based Credit Card Fraud Detection

![Python](https://img.shields.io/badge/Python-3.11-blue)

![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)

![XGBoost](https://img.shields.io/badge/XGBoost-Model-green)

![License](https://img.shields.io/badge/License-MIT-lightgrey)

![Status](https://img.shields.io/badge/Status-Completed-success)

## Overview

Credit card fraud remains one of the most significant challenges faced by financial institutions due to the increasing volume and complexity of digital transactions. This project develops and evaluates machine learning models for detecting fraudulent credit card transactions using a large-scale dataset containing over 1.8 million transactions.

The project follows the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology, covering the complete machine learning pipeline from data understanding and preprocessing to feature engineering, model development, optimization, and evaluation.

This project evaluates both supervised classification and anomaly detection techniques to compare their effectiveness in identifying fraudulent transactions.

---

## Project Highlights

• 1.8M+ transactions

• CRISP-DM Framework

• 5 Machine Learning Models

• XGBoost F1-score: 0.816

• ROC-AUC: 0.994

• Out-of-Time Validation

---

## Business Problem

Financial institutions process millions of transactions every day, making manual fraud detection impractical.

The objective of this project is to develop a machine learning framework capable of accurately identifying fraudulent transactions while minimizing false alarms and maintaining strong performance on previously unseen transaction data.

Key challenges addressed include:

- Highly imbalanced transaction data
- Complex customer spending behavior
- Detection of evolving fraud patterns
- Model generalization to future transactions

---

## Dataset

**Dataset:** Kaggle Credit Card Fraud Detection Dataset

Dataset Characteristics:

- Over **1.8 million** transactions
- Binary classification problem
- Legitimate and fraudulent transactions
- Temporal transaction records
- Customer, merchant, geographic, and transaction information

Target Variable:

- `is_fraud`
    - 0 = Legitimate Transaction
    - 1 = Fraudulent Transaction

---

## Methodology

The project follows the CRISP-DM framework.

### Data Preparation

- Data cleaning
- Missing value handling
- Winsorization of numerical variables
- Random Undersampling for class imbalance
- One-Hot Encoding
- Principal Component Analysis (PCA)

### Feature Engineering

Developed behavioral and contextual features including:

- Spending-based features
- Temporal features
- Merchant behavior
- Geographic information
- Transaction frequency
- Customer behavioral indicators

### Machine Learning Models

#### Supervised Learning

- Logistic Regression
- XGBoost

#### Unsupervised Learning

- Isolation Forest
- Local Outlier Factor (LOF)
- One-Class Support Vector Machine (SVM)

### Model Optimization

- Grid Search Hyperparameter Tuning
- Threshold Optimization
- Feature Selection
- Out-of-Time (OOT) Validation

---

## Results

Among all evaluated models, the **Tuned XGBoost** classifier achieved the strongest overall performance.

| Metric | Tuned XGBoost |
|---------|--------------:|
| Precision | **0.886** |
| Recall | **0.757** |
| F1-score | **0.816** |
| ROC-AUC | **0.994** |
| Average Precision | **0.874** |
| OOT F1-score | **0.792** |

### Key Findings

- Feature engineering substantially improved fraud detection performance.
- Supervised learning consistently outperformed anomaly detection methods.
- XGBoost demonstrated excellent generalization through Out-of-Time validation.
- Isolation Forest provided the strongest anomaly detection performance among the unsupervised models and can serve as a complementary screening tool.

---

## Tech Stack

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn

### Development Environment

- Jupyter Notebook

### Methodology

- CRISP-DM

---

## Future Improvements

Potential improvements include:

- Evaluate deep learning architectures such as LSTM and Transformer models.
- Investigate graph-based fraud detection techniques.
- Compare additional class imbalance handling strategies such as SMOTE and ADASYN.
- Explore logarithmic transformations as an alternative to winsorization for skewed numerical variables.
- Develop hybrid frameworks combining supervised classification with anomaly detection.
- Implement real-time fraud detection and concept drift adaptation.
- Validate the framework using datasets from multiple financial institutions.
