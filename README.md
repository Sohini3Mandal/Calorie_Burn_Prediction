# 🔥 Calorie Burn Prediction


**Author:** Sohini Mandal

**Live App:** [https://calorieburnprediction-nbj9yjsmyufg7xxvr9syzu.streamlit.app/](https://calorieburnprediction-nbj9yjsmyufg7xxvr9syzu.streamlit.app/)

---

## Overview

End-to-end machine learning project that estimates **calories burned during structured exercise sessions** using demographic, anthropometric, and exercise-related features. The project covers data exploration, model comparison, validation, and deployment via a Streamlit web application.

---

## Dataset

* **Source:** Kaggle (`Calories.csv`)
* **Size:** 15,000 observations
* **Features:** Gender, Age, Height, Weight, Duration, Heart Rate, Body Temperature
* **Target:** Calories burned
* User ID removed; no missing values; no duplicate records
* Intended for **methodological demonstration**, not real-world physiological inference

---

## Methodology

* 80–20 train–test split
* One-hot encoding (Gender) + feature standardization
* Models: Linear, Ridge, Lasso, Random Forest, Gradient Boosting, XGBoost, **SVR**
* Hyperparameter tuning via **5-fold cross-validation**
* Metrics: R², RMSE, MAE

---

## Results

* Linear models: R² ≈ 0.97
* Nonlinear models performed better
* **Support Vector Regression (SVR)** achieved best performance

  * **Test R²:** **0.9996**
  * Very low prediction error

---

## Deployment

The trained SVR model is deployed as a **Streamlit web application** for real-time calorie burn estimation.

👉 **Live App:** [https://calorieburnprediction-nbj9yjsmyufg7xxvr9syzu.streamlit.app/](https://calorieburnprediction-nbj9yjsmyufg7xxvr9syzu.streamlit.app/)

---

## Repository Structure

```
Calorie_Burn_Prediction/
│
├── Calorie Burn Prediction (Report).pdf   # Detailed project report
├── CalorieBurnPrediction(Notebook).ipynb  # Model training & analysis
├── Calories.csv                           # Dataset
├── best_model.pkl                         # Trained SVR model
├── scaler.pkl                             # StandardScaler object
├── feature_names.pkl                      # Feature schema
├── prediction_app.py                      # Streamlit application
├── requirements.txt                       # Dependencies
└── README.md                              # Project documentation

```
---
