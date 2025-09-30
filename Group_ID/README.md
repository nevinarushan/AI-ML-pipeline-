# Credit Card Fraud Detection Preprocessing

## Overview

This project focuses on the preprocessing of a credit card fraud detection dataset. The goal is to clean and prepare the data for machine learning modeling. The preprocessing pipeline includes handling missing values, encoding categorical variables, outlier treatment, feature engineering, and balancing the dataset.

## Dataset

The dataset used is the "Credit Card Fraud Detection" dataset, which contains transactions made by European cardholders in September 2013. It presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

The dataset is located in the `data/raw/` directory.

## Group Member Roles

| IT Number    | Name             | Role                               |
|--------------|------------------|------------------------------------|
| IT24103829   | Kishan Ahamed    | Handling Missing Values            |
| IT24103851   | Abhinaya Kumar   | Encoding Categorical Variables     |
| IT24103834   | Lafry            | Outlier Handling                   |
| IT24102335   | Nevin Nijanthan  | Feature Engineering & Selection    |
| IT24103022   | Indhuwara        | Train/Test Split & Scaling         |
| IT24103843   | Sandali          | SMOTE (Class Balancing)            |

## How to Run

1.  Ensure you have the required libraries installed. You can install them using the `requirements.txt` file:
    ```
    pip install -r requirements.txt
    ```
2.  The main integrated pipeline is available in the `notebooks/group_pipeline.ipynb` notebook. You can run this notebook to execute the entire preprocessing workflow.
3.  Individual contributions and the specific preprocessing step are detailed in the respective notebooks within the `notebooks/` directory.
