# AI-Driven Customer Intelligence System

## Problem Statement
A telecom company wants to understand its customer base without any predefined labels. They need to identify valuable segments, at-risk customers, and tailor marketing strategies accordingly.

## Dataset
- **Source**: IBM Telco Customer Churn (Kaggle)
- **Records**: 7,043 customers
- **Features**: 21 (demographics, services, account info)
- **Target**: Not used (unsupervised)

## Algorithms Used
- K-Means
- Hierarchical Clustering (Agglomerative)
- DBSCAN
- Gaussian Mixture Model (GMM)

## How to Run
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Place the raw dataset in `data/raw/` (download from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn))
4. Run the pipeline: `python main.py`

## Key Results
- **Optimal clusters**: 4 (selected via Silhouette Score and Davies-Bouldin Index)
- **Best algorithm**: K-Means (highest silhouette score, interpretable clusters)
- **Business insights**:
  - Cluster 0: High-value loyal customers – target with premium plans
  - Cluster 1: Short-term, high-spend customers – at risk, offer retention incentives
  - Cluster 2: Low-engagement customers – cross-sell basic services
  - Cluster 3: Senior, high-tenure customers – promote add-ons

## Sample Visualizations
![PCA Cluster Visualization](results/clusters_2d_pca.png)
