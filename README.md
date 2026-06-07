# Customer Segmentation Using K-Means Clustering

## Live Demo

---

## Project Overview

Understanding customer behavior is essential for businesses seeking to improve marketing effectiveness, increase customer retention, and maximize revenue. Rather than treating all customers the same, businesses can use customer segmentation to identify groups with similar purchasing patterns and target them with personalized strategies.

This project uses K-Means Clustering, an unsupervised machine learning algorithm, to segment mall customers based on demographic and spending characteristics. The model automatically discovers meaningful customer groups without requiring predefined labels.

The final solution identifies six unique customer segments and provides visual insights through PCA-based cluster visualization.

---

## Business Problem

Retail businesses often struggle to understand how different customers behave.

Questions such as:

* Which customers spend the most?
* Which customers generate the highest value?
* Which customers are at risk of low engagement?
* Which customer groups should receive targeted promotions?

can be addressed through customer segmentation.

The goal of this project is to identify distinct customer groups that can support data-driven marketing and customer relationship strategies.

---

## Dataset

Mall Customer Segmentation Dataset

Features:

* Customer ID
* Gender
* Age
* Annual Income (k$)
* Spending Score (1-100)

Target:

This is an unsupervised learning problem, therefore no target variable exists.

---

## Machine Learning Workflow

### Data Preparation

* Loaded customer transaction dataset
* Selected numerical customer attributes
* Standardized features using StandardScaler
* Prepared data for clustering analysis

### Feature Scaling

Standardization was applied to:

* Age
* Annual Income
* Spending Score

Scaling ensures that features contribute equally during distance calculations used by K-Means.

---

## Determining the Optimal Number of Clusters

To identify the most appropriate number of customer segments, Silhouette Analysis was performed.

The silhouette score evaluates:

* Cluster cohesion
* Cluster separation
* Overall clustering quality

Multiple cluster configurations were tested before selecting:

### Optimal Number of Clusters: 6

---

## Model Development

Algorithm:

### K-Means Clustering

Parameters:

* n_clusters = 6
* random_state = 42

The algorithm assigns each customer to the nearest cluster centroid and iteratively optimizes cluster boundaries.

---

## Customer Segments Identified

### Cluster 1

* High income
* High spending customers

Business Action:

* Premium offers
* Loyalty rewards
* VIP programs

### Cluster 2

* Low income
* High spending customers

Business Action:

* Promotional campaigns
* Discount targeting

### Cluster 3

* High income
* Low spending customers

Business Action:

* Upselling opportunities
* Product recommendations

### Cluster 4

* Low income
* Low spending customers

Business Action:

* Cost-efficient engagement strategies

### Cluster 5

* Average income
* Average spending customers

Business Action:

* Retention campaigns

### Cluster 6

* Younger customers with moderate spending behavior

Business Action:

* Personalized marketing initiatives

---

## Cluster Analysis

Average customer characteristics were calculated for each cluster:

| Metric         |
| -------------- |
| Age            |
| Annual Income  |
| Spending Score |

This analysis enables businesses to understand the profile of each customer segment and design targeted strategies accordingly.

---

## Dimensionality Reduction & Visualization

Principal Component Analysis (PCA) was used to reduce the dataset into two dimensions for visualization.

Benefits:

* Easier cluster interpretation
* Visual separation of customer groups
* Improved stakeholder communication

The resulting PCA visualization demonstrates the distinct customer segments identified by the clustering algorithm.

---

## Tech Stack

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Joblib

### Machine Learning

* K-Means Clustering
* StandardScaler
* Silhouette Score
* PCA

---

## Project Structure

```text
customer-segmentation/
│
├── Customer_Segmentation.ipynb
├── app.py
├── kmeans_model_for_Customer_Segmentation.pkl
├── requirements.txt
├── README.md
└── Mall_Customers.csv
```

## Results

Successfully segmented customers into six distinct groups using K-Means clustering.

Key achievements:

* Data preprocessing and feature scaling
* Optimal cluster selection using silhouette analysis
* Customer behavior segmentation
* PCA visualization
* Model serialization using Joblib
* Streamlit deployment for interactive use

---

## Future Improvements

* Interactive cluster dashboard
* Customer recommendation engine
* DBSCAN comparison
* Hierarchical clustering comparison
* Automated business insight generation
* Cloud deployment using Docker and AWS

