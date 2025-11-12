B2B Customer Churn Prediction - Bulgarian Telecom Sector
Project Overview
This repository contains a notebook for predicting business customer churn in the Bulgarian telecom sector. Churn prediction is vital for telecom providers, especially when dealing with B2B accounts that represent significant revenue.

Project Goal: Forecast which business clients are likely to terminate their telecom contracts using machine learning.

Dataset: Contains ~8,000 business accounts from a Bulgarian telecom company. Each record is labeled as churned or retained. Source

Workflow Outline: 

Introduction

Overview and importance of B2B churn.

Key differences from B2C churn.

Dataset Overview

Loads the CSV file "Baza customer Telecom v2.csv", outlines features, and inspects class distribution.

Data Cleaning & Preprocessing

Drops ID columns and handles missing data.

Fills NAs, removes columns with too many missing values, and encodes categorical variables.

Detects and removes duplicate entries.

Exploratory Data Analysis (EDA)

Investigates churn distribution and segmentation.

Examines boxplots, correlation heatmaps, and churn “hotspots” across segments.

Feature Engineering

One-hot encodes categorical variables.

Standard scales numerical features.

Model Building & Evaluation

Splits the data for training/testing.

Addresses class imbalance using KMeansSMOTE oversampling.

Compares models: Logistic Regression, Random Forest, and SVM.

Evaluates using accuracy, F1-score, ROC-AUC, and confusion matrix.

Insights & Recommendations

Discusses drivers of churn and provides actionable segmentation analysis.

Emphasizes complexity of churn and recommends tree-based ensemble methods for prediction.

Key Insights
Churn Imbalance: Only 6-8% of B2B customers churn. Handling class imbalance (resampling, class weights) is critical.

Segmentation Hotspots: Highest churn risk in small-medium business accounts within mid-to-high value segments.

Revenue Patterns: Churn isn’t explained by revenue alone—complex behavioral and contractual patterns are relevant.

Best Models: Tree-based ensembles (Random Forest, XGBoost) outperform linear models due to non-linear churn drivers.

Usage Instructions
Run the Notebook: Open B2B_Customer_Churn.ipynb and execute cells sequentially.

Libraries Needed: pandas, numpy, scikit-learn, statsmodels, seaborn, matplotlib, imbalanced-learn.

Data File: Ensure "Baza customer Telecom v2.csv" is in your working directory.

Author
Rishi Koushik Sridharan
