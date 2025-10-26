# DataPreprocessing — Credit Card Fraud Detection Pipeline

This repository implements an end-to-end data preprocessing and model training pipeline for the credit card fraud detection dataset.

Dataset (relative path)
- Use the dataset from the repository root with the relative path: ./Group_ID/data/raw/creditcard.csv
- Notebooks located in Group_ID/notebooks should read the dataset with: ../data/raw/creditcard.csv
- Notebooks located in Group_ID/notebooks/modeltraining should read the dataset with: ../../data/raw/creditcard.csv

What happens in this project (high-level)

1. Data ingestion
   - The raw CSV file (creditcard.csv) is stored at Group_ID/data/raw/creditcard.csv.
   - All notebooks and scripts should use the relative paths above so the project runs on other machines without changing absolute paths.

2. Exploratory Data Analysis (EDA)
   - Notebooks in Group_ID/notebooks perform EDA: class distribution, feature histograms, correlation heatmaps, and other visual checks.
   - Generated figures are saved in results/eda_visualizations/.

3. Preprocessing and feature engineering
   - Missing value checks and handling (imputation or removal as appropriate).
   - Outlier detection and treatment using statistical methods and visual inspection.
   - Encoding categorical features (if present) and feature transformation.
   - Feature scaling / normalization (StandardScaler, MinMaxScaler) when required by models.
   - New feature creation and feature selection based on correlation and importance.
   - Train/test splitting with fixed random state for reproducibility.

4. Imbalance handling
   - The dataset is highly imbalanced. SMOTE (and variants) are used in dedicated notebooks (Group_ID/notebooks/smote.ipynb) to balance the training data before fitting supervised models.

5. Model training and evaluation (Group_ID/notebooks/modeltraining)
   - Multiple model paradigms are explored:
     - Supervised classifiers: Logistic Regression, Random Forest, XGBoost
     - Anomaly detection / unsupervised: Isolation Forest, One-Class SVM, Autoencoders
   - Typical workflow in each model notebook:
     - Load preprocessed data using the relative path ../../data/raw/creditcard.csv (from the modeltraining folder)
     - Split data into train/validation/test sets
     - Optionally apply sampling (SMOTE) on training set
     - Train model and perform hyperparameter tuning (grid search or manual tuning)
     - Evaluate using metrics suited for imbalanced classification: precision, recall, F1-score, ROC AUC, confusion matrix, and precision-recall curves
     - Save trained model artifacts under models/ and experiment outputs to results/

6. Outputs and artifacts
   - Visualizations: results/eda_visualizations/
   - Logs and experiment outputs: results/logs/ and results/outputs/
   - Saved models (when produced): models/

How to reproduce

1. Create a Python virtual environment and install dependencies from requirements.txt.
2. Ensure Group_ID/data/raw/creditcard.csv exists; use the relative path noted above when loading data from notebooks/scripts.
3. Run the notebooks in this suggested order to reproduce the preprocessing and modeling pipeline:
   - Group_ID/notebooks/missing_values.ipynb
   - Group_ID/notebooks/outlier_handling.ipynb
   - Group_ID/notebooks/encoding.ipynb
   - Group_ID/notebooks/feature_engineering.ipynb
   - Group_ID/notebooks/train_test_split.ipynb
   - Group_ID/notebooks/smote.ipynb
   - Group_ID/notebooks/modeltraining/*.ipynb

Notes about relative paths in code
- The repository contains multiple notebooks. Relative paths used in existing notebooks are:
  - Group_ID/notebooks/*  => data loaded with "../data/raw/creditcard.csv"
  - Group_ID/notebooks/modeltraining/* => data loaded with "../../data/raw/creditcard.csv"
- If you convert notebooks to scripts or move files, update the relative path accordingly. Always prefer relative paths over absolute paths for portability.

Contact / Contributors
- Project created for a group coursework. See Group_ID/README.md for per-member notes and individual notebooks.


