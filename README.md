# Credit Score Segmentation using Clustering
You are provided with sample 100K raw, transaction-level data from the Aave V2 protocol. Each record corresponds to a wallet interacting with the protocol through actions such as `deposit`, `borrow`, `repay`, `redeemunderlying`, and `liquidationcall`.

Your task is to develop a robust machine learning model that assigns a **credit score between 0 and 1000** to each wallet, based solely on historical transaction behavior. Higher scores indicate reliable and responsible usage; lower scores reflect risky, bot-like, or exploitative behavior.

Decide which features to engineer from DeFi transaction data
Implement a one-step script that generates wallet scores from a json file which contains the a small sample of user-transactions.

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

