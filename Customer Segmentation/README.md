# Customer Segmentation Using Live API Data

A project demonstrating customer clustering based on dynamic data from API endpoints, without relying on static CSV files.

---

## Overview

This project demonstrates a complete customer segmentation workflow using live API data. It uses endpoints from the [DummyJSON](https://dummyjson.com) service to fetch data, engineer customer-level features, and identify distinct behavioral clusters entirely in memory.

The goal is to simulate a more realistic data analytics pipeline where data is acquired dynamically. The process includes:

* Fetching and integrating data from multiple API endpoints.
* Engineering behavioral and demographic features.
* Applying **PCA** (Principal Component Analysis) for dimensionality reduction.
* Modeling clusters using **KMeans** and **Gaussian Mixture Models (GMM)**.
* Evaluating model performance with **Silhouette**, **Davies–Bouldin**, and **BIC** metrics.
* Profiling and visualizing the resulting customer segments.

---

## Project Objective

The primary objective is to build and execute an end-to-end unsupervised learning pipeline. This project showcases how to perform segmentation using only live API data, a workflow that more closely resembles modern, production-level data systems.

---

## Technology Stack

| Category | Libraries / Tools |
|-----------|-------------------|
| Data Ingestion | `requests`, `pandas`, `json_normalize` |
| Data Processing | `numpy`, `scikit-learn` (`SimpleImputer`, `StandardScaler`) |
| Modeling | `KMeans`, `GaussianMixture`, `PCA` |
| Evaluation | `silhouette_score`, `davies_bouldin_score`, `BIC` |
| Visualization | `matplotlib`, `seaborn` |

---

## Workflow Details

### 1. API Data Fetching
Data is pulled from the `/users` and `/carts` endpoints of the DummyJSON API. The raw JSON responses are normalized into flat tables using `json_normalize` and then merged to create a unified dataset of user demographics and their associated purchasing behaviors.

### 2. Feature Engineering
A set of behavioral features is constructed from the raw data to describe each customer, including:
* Order frequency (`n_orders`)
* Total and discounted spend
* Average basket size, item price, and discount rate
* Product diversity (number of unique products purchased)
* Key demographic attributes (age, gender, location)

### 3. Preprocessing
The engineered dataset is prepared for modeling. This step involves handling any missing values (using `SimpleImputer`), standardizing all numerical features (using `StandardScaler`), and applying one-hot encoding to categorical features like country.

### 4. Multivariate Analysis
Correlation heatmaps and **PCA** (Principal Component Analysis) are used to explore relationships between variables and to reduce the dimensionality of the feature space before modeling.

### 5. Modeling
Two different unsupervised clustering algorithms are applied:
* **KMeans:** To find compact, well-defined clusters.
* **Gaussian Mixture Model (GMM):** To provide a probabilistic segmentation.

Model hyperparameters (specifically the number of clusters) are tuned by evaluating **Silhouette**, **Davies–Bouldin**, and **BIC** scores.

### 6. Profiling and Interpretation
Each resulting cluster is analyzed to understand its unique profile based on spending habits, basket composition, and demographics. This analysis leads to assigning descriptive labels to the segments, such as:
* *High-Value Frequent Shoppers*
* *Big-Ticket Occasional Buyers*
* *Budget-Conscious Loyalists*
* *Low-Value Customers*

---

## Potential Insights and Applications

The resulting segments can help:
* Identify and differentiate between high-value and price-sensitive customer groups.
* Understand distinct patterns in shopping frequency and product diversity.
* Provide a data-driven foundation for targeted marketing campaigns, personalization efforts, and churn prediction models.

---

## How to Run

1.  Clone the repository or open the notebook in **Google Colab / JupyterLab**.
2.  Install dependencies:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn requests
    ```
