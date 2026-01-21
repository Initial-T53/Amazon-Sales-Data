# Amazon Sales Data Readme

# Objective:
Segment e-commerce customers into distinct behavioral groups to support targeted marketing, personalization and retention strategies.

Clustering will be performed in two ways:
1: Purchase-behavior clustering (overall behavior, ignoring time)

Goal: Identify customer groups based purely on what and how they buy, regardless of when they buy. 

Value (Behavioral):
- Target Promotions
- Early Identification of churn-risk customers
- Improve loyalty and retention programs
- More personalized customer experiences.

2: Seasonality-aware clustering (monthly purchasing patterns)

Goal: Cluster customers based on when they buy rather than just how much they buy.

Value (Temporal):
- Seasonal marketing campaigns
- Inventory forecasting
- Timing promotions correctly

Note:
Due to data quality limitations in the provided dataset, seasonality clustering (#2) could not be completed. The methodology is outlined, but results are not included.


# Dataset Description
- Source: Kaggle - Amazon Sales Dataset by Rohit Kumar
- Shape: 100,000 rows x 20 columns

# Methodology/ Workflow overview
- EDA
* Data Cleaning
* Missing value handling
* Outlier detection
* Initial distribution analysis

- Customer-Level Feature Engineering
* Aggregated order-level data to customer-level
*  Created Behavioral metric:
  *  Total spend
  *  Order count  
  *  Average order value
  *  Average discount rate
  *  Average quantity
  *  sunk cost

- Clustering Approaches
* KMeans for full-coverage segmentation
* HDBSCAN for density-based, behavior-driven segmentation
* PCA visualization for interpretability
* Cluster summaries and persona definitions

- Interpretation & Recommendations
* Behavioral personas for each cluster
* Marketing and retention strategies tailored to each group
* Identification of noise cluster (HDBSCAN) and guidance on handling unclustered customers.

- Seasonality Feature Engineering (Attempted)
* Monthly order percentages
* Seasonality vectors
* Not completed due to data quality issues

# Repository breakdown
Amazon-Sales-Data
- README.md
- Requirements.txt
- data/
- notebooks/
- report/

# How to run dependencies
pip install-r requirements.txt
run notebooks


# Limitations
- Inconsistent and incomplete data fields prevented reliable month-level seasonality analysis.
- Seasonality-aware clustering is not included in the final results
- Behavior Clustering had to manually correct synthetic data
