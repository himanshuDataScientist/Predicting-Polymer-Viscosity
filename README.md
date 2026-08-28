# Predicting Polymer Viscosity Using Machine Learning

## 📌 Overview

This project focuses on predicting **polymer viscosity** using Machine Learning techniques.

The goal is to analyze polymer-related data, perform data preprocessing and feature engineering, and develop regression models capable of accurately predicting viscosity on unseen data.

Several regression models were evaluated, including **Linear Regression, Random Forest Regressor, and Gradient Boosting**. Hyperparameter optimization was also performed for the Random Forest model using `RandomizedSearchCV`.

---

## 🎯 Objectives

- Analyze and preprocess the polymer viscosity dataset
- Perform Exploratory Data Analysis (EDA)
- Identify and handle potential outliers
- Perform feature engineering
- Create polynomial and interaction features
- Train multiple regression models
- Compare model performance
- Optimize the best-performing model
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

## 🧹 Data Preprocessing

The dataset was analyzed and prepared before applying machine learning algorithms.

Potential outliers were identified in the:

`log(viscosity) in cP`

feature.

Winsorization was applied using the **0.5th and 99.5th percentiles** to reduce the influence of extreme values.

Further investigation can be performed to determine whether this approach and these percentile thresholds are optimal.

---

## ⚙️ Feature Engineering

Feature engineering was performed to help the models capture additional relationships within the dataset.

Some of the engineered features include:

- `interaction_polymer_NaCl`
- `polymer_squared`
- Polynomial features
- Interaction features

Correlation analysis was performed to understand the relationship between the engineered features and the target variable.

---

## 🤖 Machine Learning Models

The following regression models were evaluated:

### 1. Linear Regression

Linear Regression was used as a baseline model.

| Metric | Score |
|---|---:|
| R² | 0.2778 |
| MSE | 84504.2876 |
| RMSE | 290.6962 |

---

### 2. Random Forest Regressor

Random Forest performed significantly better than the Linear Regression baseline.

#### Validation Performance

| Metric | Score |
|---|---:|
| R² | 0.9947 |
| MSE | 620.8497 |
| RMSE | 24.9169 |

#### Test Performance

| Metric | Score |
|---|---:|
| R² | **0.9307** |
| MSE | **2013.3289** |
| RMSE | **44.8701** |

---

### 3. Gradient Boosting

Gradient Boosting also demonstrated strong predictive performance.

| Metric | Score |
|---|---:|
| R² | 0.9939 |
| MSE | 712.8910 |
| RMSE | 26.7000 |

---

## 📊 Model Performance

| Model | R² | MSE | RMSE |
|---|---:|---:|---:|
| Linear Regression | 0.2778 | 84504.2876 | 290.6962 |
| Random Forest | **0.9307** | **2013.3289** | **44.8701** |
| Gradient Boosting | 0.9939 | 712.8910 | 26.7000 |

**Note:** The Random Forest result shown is the held-out test performance, while the reported Gradient Boosting result should be interpreted according to the dataset split used during its evaluation.

---

## 🔧 Hyperparameter Optimization

`RandomizedSearchCV` was used to optimize the Random Forest Regressor.

The best hyperparameters obtained were:

```python
{
    'n_estimators': 200,
    'min_samples_split': 2,
    'min_samples_leaf': 1,
    'max_depth': 30
}
