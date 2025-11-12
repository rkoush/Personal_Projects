B2B Customer Churn Prediction – Bulgarian Telecom Sector 🇧🇬

A data science project to identify and predict customer churn among B2B accounts.

📖 Project Overview

This repository contains a comprehensive Jupyter notebook for predicting business customer churn in the Bulgarian telecom sector. Proactively identifying at-risk B2B accounts is vital for revenue protection, as these clients often represent a significant portion of a telecom provider's income.

🎯 Project Goal: To forecast which business clients are at a high risk of terminating their telecom contracts, using machine learning to enable targeted retention strategies.

📊 Dataset: The analysis is based on a dataset of approximately 8,000 business accounts from a Bulgarian telecom company. Each record is labeled as either churned or retained. (Source: Kaggle)

🚀 Workflow Outline

This project follows a structured data science workflow, from data ingestion to actionable insights.

Introduction

Overview and importance of B2B churn.

Key differences from B2C churn (e.g., contract value, relationship complexity).

Data Cleaning & Preprocessing

Drops irrelevant ID and high-NA columns.

Handles missing data through imputation and removal.

Encodes categorical variables.

Detects and removes duplicate entries.

🔬 Exploratory Data Analysis (EDA)

Investigates the overall churn distribution.

Analyzes churn behavior across different customer segments.

Examines boxplots, correlation heatmaps, and churn "hotspots."

Feature Engineering

One-hot encodes categorical variables for modeling.

Applies standard scaling to numerical features.

🤖 Model Building & Evaluation

Splits the data into training and testing sets.

Addresses significant class imbalance using KMeansSMOTE oversampling.

Compares three baseline models: Logistic Regression, Random Forest, and SVM.

Evaluates models using Accuracy, F1-Score, ROC-AUC, and the Confusion Matrix.

📈 Insights & Recommendations

Discusses the primary drivers of churn identified by the models.

Provides actionable segmentation analysis.

Recommends tree-based ensemble methods for future prediction.

💡 Key Insights

Highly Imbalanced Data: Churn is a rare event, with only 6-8% of B2B customers churning. This makes class imbalance handling (e.g., resampling, class weights) the most critical step for a successful model.

Segmentation Hotspots: Churn risk is not uniform. It is heavily concentrated among small-to-medium business accounts that are classified in mid-to-high value CRM segments.

Complex Churn Drivers: Revenue alone is not a strong predictor of churn. The analysis points to complex behavioral and contractual patterns that are better captured by non-linear models.

Model Performance: Tree-based ensembles (like Random Forest) and boosting algorithms (like XGBoost) are shown to outperform linear models (like Logistic Regression) due to their ability to capture these complex, non-linear relationships.

🛠️ Usage Instructions

Run the Notebook

Open B2B_Customer_Churn.ipynb in a Jupyter environment.

Execute the cells sequentially from top to bottom.

Required Libraries

Ensure you have the following Python libraries installed:

pandas
numpy
scikit-learn
statsmodels
seaborn
matplotlib
imbalanced-learn


Data File

The notebook requires the dataset file Baza customer Telecom v2.csv to be in the same working directory to run successfully.

👤 Author

Rishi Koushik Sridharan
