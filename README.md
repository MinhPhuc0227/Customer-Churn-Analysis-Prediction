# Customer Churn Analysis & Prediction

## Overview

This project analyzes customer behavior and develops a machine learning model to predict customer churn using the Telco Customer Churn dataset.

The project aims to identify key factors associated with customer churn and provide business insights that can support customer retention planning.

## Objectives

- Analyze customer characteristics and churn patterns
- Identify key factors associated with customer churn
- Compare and evaluate different machine learning models
- Select an appropriate model for churn prediction
- Translate analytical findings into customer retention recommendations

## Dataset

The dataset contains **7,043 customer records** with **21 attributes** covering customer information, subscribed services, account details, payment information, and churn status.

**Source:** [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## Analysis Process

### 1. Data Preparation
- Data cleaning and preprocessing
- Handling missing and inconsistent values
- Feature transformation and encoding
- Feature scaling

### 2. Exploratory Data Analysis
- Analyzed customer characteristics and churn patterns
- Visualized relationships between customer attributes and churn
- Identified potential factors associated with customer churn

### 3. Feature Engineering
- Encoded categorical variables
- Standardized numerical features
- Prepared features for machine learning models

### 4. Model Development & Evaluation

Evaluated **9 machine learning models** using **5-fold cross-validation**:

- Logistic Regression
- Decision Tree
- Random Forest
- AdaBoost
- Gradient Boosting
- XGBoost
- LightGBM
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

Models were evaluated using classification performance metrics, including Accuracy, F1-Score, Confusion Matrix, and ROC-AUC.

## Results

**Logistic Regression** was selected as the optimal model, achieving approximately **80% average accuracy**.

The model also achieved an **F1-Score of 0.598 for the Churn class**.

### Key Churn Factors

The analysis identified several important factors associated with customer churn:

- Contract type
- Customer tenure
- Monthly charges

These findings provide a basis for identifying customers with a higher risk of churn.

## Business Insights

Based on the analysis, customer retention strategies can focus on customers with higher churn risk by considering factors such as contract type, tenure, and monthly charges.

The findings can support businesses in identifying at-risk customers and developing targeted retention strategies.

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab
