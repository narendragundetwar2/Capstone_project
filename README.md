# Customer Segmentation

## 1) Project Title
**Customer Segmentation**

---

## 2) Problem Statement

A company has collected large volumes of customer data but does not know:
- Who their most valuable customers are
- Which customers are likely to churn
- Which group spends the most
- Which group responds better to offers

There are no labels provided. We must apply unsupervised learning to identify meaningful segments and provide business recommendations.

---

## 3) Dataset Description

- **Source**: IBM Telco Customer Churn (Kaggle)
- **Records**: 7,043 customers
- **Features**: 21 attributes

**Features Include:**
- Demographics: gender, SeniorCitizen, Partner, Dependents
- Services: PhoneService, InternetService, OnlineSecurity, TechSupport, StreamingTV
- Account Information: tenure, Contract, PaymentMethod, MonthlyCharges, TotalCharges

---

## 4) Algorithms Used

- **K-Means**: Partitions data into K clusters by minimizing within-cluster variance
- **DBSCAN**: Density-based clustering that groups points closely packed together
- **Hierarchical Clustering**: Builds tree of clusters by merging closest pairs

---

## 5) How to Run Project

```bash
# Install required packages
pip install -r requirements.txt

# Run the complete pipeline
python main.py
```

**Requirements:**
- Python 3.8+
- Download dataset from Kaggle and place in `data/raw/`

---

## 6) Key Results

### Number of Clusters Found: **4**

### Best Algorithm: **K-Means**
- Silhouette Score: 0.324
- Davies-Bouldin Index: 1.124

### Business Insights

| Cluster | Type | Characteristics | Strategy |
|---------|------|-----------------|----------|
| 0 | Premium Loyal | Long tenure, high spend, low churn | Loyalty program |
| 1 | At-Risk High Spenders | New, highest monthly, 45% churn | Retention campaign |
| 2 | Budget Conscious | Low spend, basic services | Cross-sell bundles |
| 3 | Senior Segment | Senior citizens, stable | Senior-friendly plans |

---




## 7. Sample Visualizations

### Elbow Method Graph

Used to determine the optimal number of clusters.

Example:

```
Number of Clusters (K) vs Within-Cluster Sum of Squares
```

### Customer Segmentation Scatter Plot

A scatter plot showing different clusters of customers based on:

* Annual Income
* Spending Score

Each cluster is represented by different colors, with cluster centroids highlighted.

---

