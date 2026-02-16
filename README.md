Machine Learning: Classification and Regression

This repository contains three machine learning projects covering both classification and regression tasks. The work focuses on structured preprocessing, manual hyperparameter tuning, cross-validation, and performance evaluation.

Repository Structure

1_manual_classification.ipynb – Decision Tree and Gaussian Naive Bayes implementation

2_comparison_of_classifiers.ipynb – Model comparison and evaluation

3_regression.ipynb – Linear Regression and Decision Tree Regression

Breast Cancer Classification
Dataset

The classification task uses the Wisconsin Diagnostic Breast Cancer dataset.

Each observation represents a patient case with 30 numerical features describing properties of cell nuclei (e.g., radius, texture, area, smoothness, concavity).

The goal is to classify tumors as:

Malignant (1)

Benign (0)

Methodology

Removed non-predictive ID column

Encoded target variable

80/20 stratified train-test split

5-fold cross-validation

Manual hyperparameter tuning

Models
Decision Tree (manually tuned)

Optimized using F1-score

Gaussian Naive Bayes (manually tuned)

Tuned var_smoothing parameter

Test Results
Model	Accuracy	Precision	Recall	F1
GaussianNB	0.9386	0.9730	0.8571	0.9114
Decision Tree	0.9298	1.0000	0.8095	0.8947

Both models perform strongly. GaussianNB achieves a better balance between precision and recall, making it the preferred model in this context.

Real Estate Price Prediction
Dataset

The regression task predicts house price per unit area using location and property-related features such as:

House age

Distance to MRT station

Number of convenience stores

Latitude and longitude

Non-predictive ID columns were removed during preprocessing.

Methodology

80/20 train-test split

5-fold cross-validation

Median imputation and scaling (for linear regression)

Manual hyperparameter tuning for Decision Tree Regressor

Models and Results
Model	R²	MAE	MSE
Decision Tree	0.7544	4.73	41.20
Linear Regression	0.6811	5.31	53.50

The Decision Tree Regressor outperforms Linear Regression, indicating non-linear relationships between features and house prices.
