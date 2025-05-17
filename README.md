# 🛍️ Customer Segmentation with K-Means Clustering

This project applies K-Means Clustering to segment customers in a retail shopping mall based on their demographic and behavioral attributes. The insights from this analysis can help businesses develop targeted marketing strategies, improve engagement, and optimize product offerings.

---

## 📌 Business Objective

To identify distinct customer segments using unsupervised learning, enabling the retail mall to:

- Personalize campaigns for high-value customers
- Design age/income-specific promotions
- Identify under-engaged groups for retention
- Optimize product placement and loyalty programs

---

## 🧾 Dataset

The dataset contains 200 customer records with the following features:

- `CustomerID`
- `Gender`
- `Age`
- `Annual Income (k$)`
- `Spending Score (1-100)`

📂 **Source**: [Mall Customer Dataset](https://github.com/kennedykwangari/Mall-Customer-Segmentation-Data/blob/master/Mall_Customers.csv)

---

## 🧠 Methodology

### 1. Data Preprocessing
- Loaded dataset using Pandas
- Selected numerical features: Age, Annual Income, Spending Score
- Applied StandardScaler for normalization

### 2. Elbow Method
- Calculated inertia for k = 1 to 10
- Plotted Elbow Curve to identify the optimal number of clusters

### 3. Silhouette Analysis
- Calculated silhouette scores for k = 2 to 10
- Identified peak score to evaluate clustering quality

### 4. Final K-Means Clustering
- Chose `k = 5` for final segmentation
- Visualized clusters in 2D using Age vs. Spending Score

---

## 📊 Results

| Cluster | Avg Age | Avg Income | Avg Spending Score | Insight |
|--------|---------|------------|--------------------|---------|
| 0 | ~56 | ~54k | ~49 | Older, moderate spenders |
| 1 | ~33 | ~86k | ~82 | Young, high-income, high spenders |
| 2 | ~25 | ~41k | ~62 | Young, moderate-income, impulsive shoppers |
| 3 | ~46 | ~27k | ~18 | Middle-aged, low-income, cautious |
| 4 | ~40 | ~86k | ~19 | Middle-aged, high-income, low engagement |

---

## 🛠️ Tools & Libraries

- Python (Pandas, NumPy)
- Scikit-learn
- Matplotlib, Seaborn
- Google Colab / Jupyter Notebook

---

## 📝 Interpretation

- **Cluster 1** is ideal for luxury marketing campaigns.
- **Cluster 4** represents under-utilized high-income customers—target for re-engagement.
- **Cluster 3** may benefit from discount-driven promotions or essential bundles.

---

## 📁 How to Run

1. Clone this repository
2. Install required packages:
   ```bash
   pip install pandas matplotlib seaborn scikit-learn
