# Multiclass Network Intrusion Detection Using Machine Learning

## Overview

This project investigates the use of machine learning for **multiclass network intrusion detection** using the UNSW-NB15 dataset.

The main objective was to compare four machine learning approaches for classifying network traffic into different categories of normal and malicious activity. To ensure a consistent comparison, **Recursive Feature Elimination (RFE)** was used to select a common set of 10 features, which were then used as inputs for all four models.

The models evaluated were:

- Decision Tree
- Random Forest
- XGBoost
- Multi-Layer Perceptron (MLP)

The models were evaluated using **accuracy, precision, recall, and F1 score**.

---

## Dataset

The project uses the **UNSW-NB15 network intrusion detection dataset**, which contains network traffic records representing normal activity and multiple categories of attacks.

The dataset was preprocessed by:

- Removing unnecessary columns
- Handling missing values
- Removing duplicate records
- Converting categorical features into numerical representations
- Preparing the attack category as the multiclass target

The `id` and binary `label` columns were removed, while `attack_cat` was used as the classification target.

> **Dataset note:** The `intrusion.csv` file is included in this repository only if its redistribution is permitted. If the dataset is not included, it should be obtained separately and placed in the project directory before running the notebook.

---

## Methodology

The project followed the following workflow:

```text
UNSW-NB15 Dataset
        │
        ▼
Data Cleaning & Preprocessing
        │
        ▼
Categorical Encoding
        │
        ▼
Recursive Feature Elimination (RFE)
        │
        ▼
10 Selected Features
        │
        ▼
70/30 Train-Test Split
        │
        ├──────────────┬──────────────┬──────────────┐
        ▼              ▼              ▼              ▼
 Decision Tree   Random Forest     XGBoost          MLP
        │              │              │              │
        └──────────────┴──────────────┴──────────────┘
                       │
                       ▼
                 Model Evaluation
