# 🏆 Machine Learning Hackathon: Insurance Charges Prediction

---

## 🧠 Hackathon Overview
This project was completed as part of a **Machine Learning Hackathon**, where the goal was to **train datasets for both classification and regression problems**.  

In this task, we focused on a **regression problem**: predicting **medical insurance charges** for individuals based on personal and health-related features.

---

## 📋 Dataset Features

| Column   | Description |
|----------|-------------|
| age      | Age of the individual (in years) |
| sex      | Gender (male/female) |
| bmi      | Body Mass Index (BMI) |
| children | Number of children/dependents |
| smoker   | Smoking status (yes/no) |
| region   | Residential area (northeast, southeast, southwest, northwest) |
| charges  | Insurance charges (target variable) |

---

## 🔹 Problem Statement
During the hackathon, the challenge was to **predict insurance charges** accurately using the provided dataset features.  
The objective was to **build a regression model** that could estimate insurance costs for new individuals.

---

## 🛠️ Data Preparation
- Dropped **low-correlation columns**: `sex` and `region`.  
- Encoded **categorical feature** `smoker` to numeric format.  
- Split dataset into **training and test sets** (80%-20%).  

**Key Features Used for Modeling:**  
- Age  
- BMI  
- Number of children  
- Smoker status  

---

## 📈 Model Training & Selection
Multiple regression models were tested, including:  
- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- Gradient Boosting Regressor ✅ Best performer  
- Support Vector Regressor  

**Gradient Boosting Regressor Metrics:**

| Metric | Value | Interpretation |
|--------|-------|----------------|
| R² Score | 85.85% | High predictive accuracy (~86% variance explained) |
| MAE      | 0.206  | Average prediction error |
| RMSE     | 0.362  | Standard deviation of prediction errors |

**Single Row Prediction Example:**

| Row | Predicted Value | Real Value |
|-----|----------------|------------|
| 142 | 10.627         | 10.733     |

---

## 🧠 Key Findings
- **Smoking status** and **age** have the strongest influence on insurance charges.  
- BMI and number of children slightly affect charges.  
- Sex and region have negligible effect.  
- Gradient Boosting Regressor provides the **highest accuracy** among tested models.

---

## ✅ Conclusion
- Successfully solved a **regression problem** for predicting medical insurance charges as part of the hackathon.  
- The model can **accurately estimate insurance costs** for new individuals.  
- Feature selection improved model performance by removing irrelevant columns.

---

## 🖥️ Final Python Code (Gradient Boosting Regressor)

```python
# Gradient Boosting Regressor Code (same as before)
