# AI-CodingChallange
# Credit Score Segmentation using Clustering

This project focuses on deriving **credit score categories** using **unsupervised learning (KMeans clustering)** and analyzing the **feature importance** to simulate a scoring system from anonymized user behavior and online trend metrics.

---


## ✅ Workflow Summary

### 1. **Data Preprocessing**
- data cleaning & feature engineering
- dropped highly correlated and redundent features
- created a compressed df based on present parameters
- feature scaling.

### 2. **Clustering**
- Applied **KMeans Clustering** with optimal `k=5`, determined using:
  - **Silhouette Score**
  - **Elbow Method**

### 3. **Cluster Profiling**
- Analyzed each cluster's distribution and visualization.
- Labelled clusters as :
- Cluster	Description	 Name
0	:Low activity, low diversity, moderate negative presence	💤 Dormant Negatives
1	:Slightly active, high negative trend & presence	🔻 Negatively Trending
2	:Very low everything, almost silent	🚫 Inactive Negatives
3	:High activity, high diversity, positive presence	🌟 Active & Positive Influencers
4	:Near zero activity/diversity, high negative trend, no presence	👻 Shadow Negatives

### 4. **Feature Weighting**
-weighted each datapoint to a weight and predicted credit scores

