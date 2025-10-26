# Credit Card Fraud Detection Project

## Overview

This project implements a complete pipeline for credit card fraud detection using machine learning. It covers data preprocessing, exploratory data analysis, model training, and evaluation.

## Dataset

The dataset used is the "Credit Card Fraud Detection" dataset, containing transactions made by European cardholders in September 2013. It is highly imbalanced, with only 492 frauds out of 284,807 transactions. The dataset is located in the `data/raw/` directory.

## Preprocessing Steps

The preprocessing pipeline includes:
- Handling missing values
- Encoding categorical variables
- Outlier detection and treatment
- Feature engineering and selection
- Train/test split and feature scaling
- Balancing the dataset using SMOTE

Each step is implemented in a dedicated notebook by different group members. The integrated workflow is available in `notebooks/group_pipeline.ipynb`.

## Exploratory Data Analysis (EDA)

EDA is performed to visualize class distribution, feature correlations, and the effects of preprocessing. Visualizations are saved in `results/eda_visualizations/`.

## Model Training

Multiple machine learning models are trained to detect fraudulent transactions:
- Logistic Regression
- Random Forest
- XGBoost
- Isolation Forest
- One-Class SVM
- Autoencoders

Model training and evaluation are performed in the `notebooks/modeltraining/` directory.


## How to Run

1.  Ensure you have the required libraries installed. You can install them using the `requirements.txt` file:
    ```
    pip install -r requirements.txt
    ```
2.  The main integrated pipeline is available in the `notebooks/group_pipeline.ipynb` notebook. You can run this notebook to execute the entire preprocessing and modeling workflow.
3.  Individual contributions and the specific preprocessing step are detailed in the respective notebooks within the `notebooks/` directory.
