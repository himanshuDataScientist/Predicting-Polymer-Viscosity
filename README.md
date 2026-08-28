# 🧪 Predicting Polymer Viscosity Using Machine Learning

## 📌 Overview

This project focuses on predicting **polymer viscosity** using Machine Learning techniques.

The goal is to analyze polymer-related data, perform data preprocessing and feature engineering, and develop regression models capable of predicting viscosity on unseen data.

Several regression models were evaluated, including **Linear Regression, Random Forest Regressor, and Gradient Boosting**. Hyperparameter optimization was performed using `RandomizedSearchCV` to improve the performance of the Random Forest model.

---

## 🎯 Objectives

- Analyze and preprocess the polymer viscosity dataset
- Perform Exploratory Data Analysis (EDA)
- Identify and handle potential outliers
- Perform feature engineering
- Create polynomial and interaction features
- Train multiple regression models
- Compare model performance
- Optimize the Random Forest model using hyperparameter tuning
- Evaluate the final model on unseen test data

---

## 🔄 Workflow

1. Data Loading
2. Data Cleaning and Preprocessing
3. Exploratory Data Analysis
4. Outlier Detection and Treatment
5. Feature Engineering
6. Train-Test Split
7. Model Training
8. Model Evaluation
9. Hyperparameter Optimization
10. Final Model Selection

---

## 📊 Dataset Overview

The dataset contains experimental measurements related to polymer solutions under different conditions.

### Target Variable

```text
log(viscosity) in cP
