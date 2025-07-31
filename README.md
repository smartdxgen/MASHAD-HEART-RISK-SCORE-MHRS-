## MASHAD-HEART-RISK-SCORE-MHRS-
## XAI for Cardiovascular Risk Prediction in Middle Eastern Populations
## Enhancing Cardiovascular Risk Prediction in Middle Eastern Populations: Explainable AI vs Conventional Models

## Overview
This repository hosts the code and resources for a study comparing Explainable AI (XAI) techniques with conventional logistic regression models to predict 10-year cardiovascular disease (CVD) risk in Middle Eastern populations. The study leverages data from the Mashhad Stroke and Heart Atherosclerotic Disorder (MASHAD) cohort and demonstrates the superiority of machine learning (CatBoost) in capturing non-linear interactions among risk factors.

## Key Features
### Comparative Analysis:Evaluates logistic regression (LR) against six ML models (CatBoost, Random Forest, etc.).
### Best-performing model:  --> CatBoost (AUC: 0.89) vs. LR (AUC: 0.70–0.72).
### Explainable AI (XAI) Integration: Uses SHAP (SHapley Additive exPlanations) to interpret model decisions and identify top risk factors (e.g., age-diabetes interactions, systolic blood pressure). Provides visualizations (force plots, summary plots) for clinical transparency.
### Optimized Feature Selection: Reduces 33 risk factors to 14 SHAP-derived features with minimal performance drop (AUC: 0.84).
### Clinical Applicability: Case studies illustrate high/low-risk predictions with actionable insights for cardiologists.

![cvd (1)](https://github.com/user-attachments/assets/b5018186-dd9a-410f-b095-a07e018482ec)

## 📜 Citation
```bibtex
@article{mhrs2025,
  title={Enhancing Cardiovascular Risk Prediction in Middle Eastern Populations: Explainable AI vs Conventional Models},
  author={Baniasadi, A, Dehghani, T. et al.},
  journal={Under Review},
  year={2025}
}
```
## Usage
### Dependencies: Python 3.8+, scikit-learn, catboost, shap, pandas.
### Reproducing Results:jupyter notebook notebooks/2_model_training.ipynb
### Key Functions  
**1. Data Preprocessing** ml_preprocessing_spliting(): Prepares data with SMOTE oversampling for handling class imbalance;Handles missing values, splits data into train/test sets; 
Applies SMOTE oversampling and feature scaling; One-hot encodes categorical variables; ml_preprocessing_spliting_no_smote(): Similar preprocessing without SMOTE. ** 2. Model Comparison** model_comparison(): Uses PyCaret to compare multiple classification models; Includes Decision Trees, Random Forest, KNN, Gradient Boosting, AdaBoost, CatBoost, Logistic Regression, and SVM; Generates performance metrics and visualizations (AUC, Precision-Recall curves, feature importance). ** 3. Model Evaluation ** ml_metrics(): Calculates comprehensive performance metrics; AUC, confusion matrix, precision, recall, F1-score, MCC, Cohen's kappa; Plots ROC curves and finds optimal classification threshold. ** 4. Visualization ** draw_heatmap(): Creates correlation heatmaps of features; Helps identify relationships between variables. **5. Model Saving ** save_model_information(): Stores model performance metrics for later comparison

## Workflow Steps
### Load and Explore Data: The notebook loads cardiovascular health data with features like age, blood pressure, cholesterol levels, etc.
### Basic data exploration shows the distribution of cardiovascular events
### Preprocess Data Choose between SMOTE or non-SMOTE preprocessing based on your needs-Handles missing values, scales features, encodes categorical variables
### Compare Models Use PyCaret's automated model comparison to identify top-performing algorithms
### Visualize model performance metrics
### Evaluate Best Model Generate detailed performance metrics for the selected model-Analyze confusion matrix and ROC curves-
### Visualize Feature Relationships  Examine correlations between features using heatmaps

## 📧 Contact
For collaborations and inquiries:  
[Dehghanit@mums.ac.ir](mailto:Dehghanit@mums.ac.ir) | [edu.dehghani@gmail.com](mailto:edu.dehghani@gmail.com)

**Keywords**: Cardiovascular Risk Prediction · Explainable AI · Middle Eastern Population · Machine Learning · Clinical Decision Support

#CardioRiskPrediction #ExplainableAI #MachineLearning #MiddleEastHealth #PreventiveMedicine #SHAP #CatBoost #ClinicalAI



