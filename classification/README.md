# 🧠 Stroke Prediction using Machine Learning

## 📋 Overview
This project predicts the likelihood of a stroke occurrence in patients based on medical and demographic features using machine learning models.  
The dataset includes information such as age, gender, hypertension, heart disease, BMI, glucose levels, and smoking habits.

## 🎯 Objective
The goal is to build and compare multiple machine learning models to determine which algorithm performs best in predicting strokes, ultimately supporting early detection and prevention.

## 🧩 Dataset Information

- **Total Rows:** 5,110  
- **Total Columns:** 12  
- **Target Column:** `stroke` (1 = stroke, 0 = no stroke)  

| Column           | Description                                      |
|-----------------|--------------------------------------------------|
| gender           | Gender of the patient                             |
| age              | Age in years                                     |
| hypertension     | 1 = patient has hypertension, 0 = otherwise     |
| heart_disease    | 1 = patient has heart disease, 0 = otherwise    |
| ever_married     | Yes/No                                           |
| work_type        | Type of work (Private, Govt_job, Self-employed, etc.) |
| Residence_type   | Urban/Rural                                     |
| avg_glucose_level| Average glucose level in blood                   |
| bmi              | Body Mass Index                                  |
| smoking_status   | Smoking habits (never smoked, smokes, formerly smoked, Unknown) |
| stroke           | Target variable                                  |

## ⚙️ Project Workflow

### 1️⃣ Data Preprocessing
- Loaded and cleaned the dataset.
- Filled missing BMI values using mean imputation.
- Label-encoded categorical variables.
- Balanced classes using SMOTE (Synthetic Minority Oversampling Technique).

### 2️⃣ Exploratory Data Analysis (EDA)
- Analyzed feature distributions and relationships.
- Visualized correlations with a heatmap.
- Examined stroke distribution by health and lifestyle factors.

### 3️⃣ Model Building
Trained multiple machine learning models:  
- Logistic Regression  
- Decision Tree  
- Random Forest 🌟  
- Gradient Boosting  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  

### 4️⃣ Model Evaluation
Evaluated each model using:  
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Confusion Matrix  

**🏆 Best Performing Model:** Random Forest Classifier  
- **Accuracy:** 94.24%  
- Balanced precision and recall  
- Outperformed all other models on test data  

## 📊 Results Summary

| Model                 | Accuracy | Precision | Recall | F1 Score |
|-----------------------|---------|-----------|-------|----------|
| Logistic Regression   | 0.7938  | —         | —     | —        |
| Decision Tree         | 0.9044  | —         | —     | —        |
| Random Forest         | 0.9424  | High      | High  | High     |
| Gradient Boosting     | 0.8751  | —         | —     | —        |
| SVM                   | 0.5111  | —         | —     | —        |
| KNN                   | 0.8077  | —         | —     | —        |

> **Note:** Exact precision/recall values may vary slightly depending on random state.

## 🧠 Confusion Matrix (Random Forest)

|                   | Predicted: No Stroke | Predicted: Stroke |
|-------------------|-------------------|-----------------|
| Actual: No Stroke | True Negatives     | False Positives |
| Actual: Stroke    | False Negatives    | True Positives  |

Visualized using Seaborn heatmap for better interpretability.

## 🧰 Libraries Used
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- imblearn  
