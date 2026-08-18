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

This project uses the UNSW-NB15 network intrusion detection dataset.

The dataset is not included in this repository. It can be obtained from the
official UNSW-NB15 dataset page:

https://research.unsw.edu.au/projects/unsw-nb15-dataset

After downloading the dataset used for this project, place the required CSV
file in the project directory and name it:

intrusion.csv

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
