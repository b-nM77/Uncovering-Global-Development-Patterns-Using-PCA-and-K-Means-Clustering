## Uncovering Global Development Patterns (2010–2020)

![Unsupervised Learning](https://img.shields.io/badge/Unsupervised%20Learning-PCA%20%2B%20KMeans-orange)
![PCA](https://img.shields.io/badge/Dimensionality%20Reduction-PCA-yellow)
![KMeans](https://img.shields.io/badge/Clustering-KMeans-red)
![World Bank](https://img.shields.io/badge/Dataset-World%20Bank%20WDI-green)
![Years](https://img.shields.io/badge/Years-2010--2020-lightgrey)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Manipulation-lightgrey?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-blue?logo=numpy)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML%20Algorithms-orange?logo=scikitlearn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-blue)

### PCA + K-Means Clustering on World Development Indicators
This project applies unsupervised machine learning to analyse a decade of global socioeconomic data. Using Principal Component Analysis (PCA) and K-Means clustering, we identify natural groupings of countries based on similarities in:
 - Economy
 - Education
 - Health
 - Infrastructure
 - Agriculture
 - Environment

The result is a clear, interpretable segmentation of world nations into meaningful development clusters.

## Data Source

This project uses openly available indicators from the World Bank Development Indicators (WDI) dataset.
All data was obtained from the curated GitHub repository:

🔗 https://github.com/light-and-salt/World-Bank-Data-by-Indicators

For this analysis, the following domain files were selected:
 - economy-and-growth.csv
 - education.csv
 - agriculture-and-rural-development.csv
 - environment.csv
 - health.csv
 - infrastructure.csv

Each category contains multiple country-level indicators. These were cleaned, filtered, and aggregated for the period 2010–2020.

##  Project Overview
The workflow of this project includes:
 - Exploratory Data Analysis (EDA)
 - Missingness and skewness inspection
 - Feature selection (final curated list of ~30 indicators)
 - Preprocessing & feature engineering
 - PCA dimensionality reduction
 - K-Means clustering
 - Visualization of global clusters in PCA space and on a world map

The aim is to uncover emerging socioeconomic patterns without using any predefined labels.

## Key Methods
1. Exploratory Data Analysis
    - Missingness analysis
    - Distribution and skewness checks
    - Correlation heatmaps
    - Domain-wise feature selection
      
2. Preprocessing & Feature Engineering
    - A full preprocessing pipeline was built including:
    - Median imputation
    - Log-transforming skewed features
    - Outlier clipping (1st–99th percentile)
    - Standardization (required for PCA & K-Means)
    - Final master dataset created with ~30 selected indicators
      
4. Unsupervised Modelling
    - PCA for dimensionality reduction
    - PCA explained variance analysis
    - 2D and 3D PCA projections
    - K-Means clustering
    - Elbow plot & silhouette score evaluation
    - Cluster visualization in PCA space
    - Choropleth world map (Plotly)
      
##  Main Findings
 ### PCA Insights
  - PC1 explains ~53% of total variance — a strong “overall development level” axis capturing income, education, infrastructure, and health.
  - PC2 captures environmental structure and natural resource dependence.
  - Together, the first 8–10 components capture ~90% of global variance.

#### Optimal Number of Clusters: 4 (Based on elbow method + silhouette scores.)

### Identified Country Clusters
 - Cluster 0 — High-Income Advanced Economies
    - Strong digital infrastructure, high GDP, aging populations, high education levels.
 - Cluster 1 — Emerging Industrializing Economies
    - Middle-income growth, improving infrastructure, transitioning from agriculture to industry/services.
 - Cluster 2 — Lower-Income Agrarian Economies
    - High rural populations, agriculture-dependent, younger demographics, lower digital access.
 - Cluster 3 — Resource-Rich Export Economies
    - High natural resource rents (oil/minerals), unique demographic/economic structures.

## Technologies Used
```bash
Python (Pandas, NumPy), Scikit-Learn, Seaborn & Matplotlib, Plotly
```

## Conclusion
This study demonstrates the effectiveness of unsupervised learning for high-dimensional socioeconomic analysis. PCA captures the major axes of variation—dominated by development level and structural economic factors—while K-Means identifies stable, well-separated clusters that correspond closely with recognised global development categories. 

The end-to-end pipeline, including preprocessing, feature engineering, dimensionality reduction, and clustering, highlights the robustness of unsupervised methods for exploratory data segmentation and multivariate pattern discovery.
