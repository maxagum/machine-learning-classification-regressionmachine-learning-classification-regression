# Machine Learning: Classification and Regression

This repository contains three applied machine learning projects covering both **classification** and **regression** tasks. The work emphasizes structured preprocessing, manual hyperparameter tuning, cross-validation, and thorough model evaluation.

---

## Repository Structure

- `1_manual_classification.ipynb`
- `2_comparison_of_classifiers.ipynb`
- `3_regression.ipynb`

---

# Breast Cancer Classification

## Dataset

The classification task uses the **Wisconsin Diagnostic Breast Cancer dataset**.

Each observation represents a patient case with 30 numerical features describing properties of cell nuclei (e.g., radius, texture, area, smoothness, concavity, symmetry).

The objective is to classify tumors as:

- **Malignant (1)**
- **Benign (0)**

---

## Methodology

- Removed non-predictive ID column  
- Encoded target variable  
- 80/20 stratified train-test split  
- 5-fold stratified cross-validation  
- Manual hyperparameter tuning  

---

## Models Implemented

### Decision Tree Classifier
- Tuned using nested loops  
- Optimized using F1-score  

### Gaussian Naive Bayes
- Tuned `var_smoothing` parameter  
- Optimized using F1-score  

---

## Test Results

| Model           | Accuracy | Precision | Recall | F1     |
|----------------|----------|-----------|--------|--------|
| GaussianNB     | 0.9386   | 0.9730    | 0.8571 | 0.9114 |
| Decision Tree  | 0.9298   | 1.0000    | 0.8095 | 0.8947 |

Both models achieve strong performance.  
GaussianNB provides a better balance between precision and recall, making it the preferred model in this context.

---

# Real Estate Price Prediction

## Dataset

The regression task predicts **house price per unit area** based on:

- Transaction date  
- House age  
- Distance to nearest MRT station  
- Number of convenience stores  
- Latitude  
- Longitude  

Non-predictive identifier columns were removed during preprocessing.

---

## Methodology

- 80/20 train-test split  
- 5-fold cross-validation  
- Median imputation  
- Feature scaling (for linear regression)  
- Manual hyperparameter tuning (Decision Tree Regressor)  

---

## Models and Results

| Model              | R²     | MAE   | MSE    |
|-------------------|--------|--------|--------|
| Decision Tree     | 0.7544 | 4.73   | 41.20  |
| Linear Regression | 0.6811 | 5.31   | 53.50  |

The Decision Tree Regressor outperforms Linear Regression, indicating non-linear relationships between features and house prices.

---

# Techniques Demonstrated

- Manual hyperparameter tuning  
- Stratified cross-validation  
- Confusion matrix analysis  
- Evaluation metrics: Accuracy, Precision, Recall, F1  
- Regression metrics: R², MAE, MSE  
- Reproducible experiments (fixed random seeds)  
