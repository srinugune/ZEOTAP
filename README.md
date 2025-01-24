# Customer Analytics: Segmentation, Lookalike Model, and Data Insights

### Overview

This project focuses on three major tasks related to customer analytics:
  Task 1: Exploratory Data Analysis (EDA) to generate meaningful insights.
  Task 2: Development of a Lookalike Model to recommend similar customers.
  Task 3: Customer Segmentation using clustering techniques.
Each task utilizes customer profile data and transaction history to deliver actionable insights for businesses.

## Key Features
**Task 1: Exploratory Data Analysis (EDA)**
**Objective:** Generate business insights by exploring and analyzing customer and transaction data.
**Highlights:**
Number of customers by region and transaction activity.
Total spending patterns and most valuable customer segments.
Time-based analysis of customer activity.
**Visualizations:**
Bar charts, line graphs, and heatmaps to represent trends and distributions.

**Task 2: Lookalike Model**
**Objective:** Build a model to recommend the top 3 similar customers for a given customer based on their profile and transaction history.
**Highlights:**
Utilizes Cosine Similarity for computing customer similarity.
Recommends similar customers with similarity scores for the first 20 customers.
**Deliverables:**
Recommendations saved in Lookalike.csv in the format: Map<CustomerID, List<(CustomerID, SimilarityScore)>>.

**Task 3: Customer Segmentation**
**Objective:** Segment customers into meaningful clusters using their profile and transaction data.
**Highlights:**
Features used: Recency (days since signup), Total Spending, and Transaction Frequency.
Clusters evaluated using DB Index and Silhouette Score.
**Deliverables:**
Cluster assignments saved in Customer_Clusters.csv.

## Project Files
**Input Data:**
Customers.csv: Contains customer profile data (e.g., CustomerID, Region, SignupDate).
Transactions.csv: Includes transaction details (e.g., TransactionID, TotalValue, TransactionDate).
products.csv:product details
Generated Files:
Task 1 Outputs:
Visualizations and insights saved in the Jupyter Notebook.
Task 2 Outputs:
Lookalike.csv: Contains top 3 similar customers for the first 20 customers.
Task 3 Outputs:
Customer_Clusters.csv: Contains cluster assignments for each customer.
Scripts:
Task_1_EDA.ipynb: Notebook for exploratory data analysis.
Task_2_Lookalike_Model.ipynb: Notebook for the Lookalike Model.
Task_3_Clustering.ipynb: Notebook for customer segmentation.

## Workflow
**Task 1: Exploratory Data Analysis**
Data Overview:
Load and clean Customers.csv and Transactions.csv.
Feature Analysis:
Insights into regions, customer activity, and spending patterns.
Time-Based Analysis:
Spending trends by month and most active customers over time.

**Task 2: Lookalike Model**
Feature Engineering:
Features used: Total Spending, Transaction Frequency, Region, and Recency.
Model Development:
Calculated pairwise Cosine Similarity between customers.
Recommendations:
Generated the top 3 similar customers for CustomerID: C0001 - C0020.

**Task 3: Customer Segmentation**
Feature Engineering:
Created features: Recency, Total Spending, and Transaction Frequency.
Preprocessed data using StandardScaler and OneHotEncoder.
Clustering:
Applied KMeans for cluster sizes from 2 to 10.
Evaluated clusters using:
DB Index: Measures cluster compactness and separation.
Silhouette Score: Measures cluster cohesion and separation.
Visualization:
Visualized clusters using scatter plots, pair plots.
Evaluation Metrics
Task 2: Lookalike Model
Cosine Similarity: Measures the similarity between customer vectors.
Recommendations saved with scores for easy interpretation.
Task 3: Clustering
DB Index: Lower values indicate better-defined clusters.
Silhouette Score: Higher values indicate well-separated clusters.
Example Final Metrics (Task 3):
DB Index: 0.85
Silhouette Score: 0.62
Visualizations
EDA:
Spending distribution and customer segmentation by region.
Time-based trends using line charts.
Lookalike Model:
Heatmap of similarity scores between customers.
Customer Segmentation:
Scatter plots showing cluster separations.

## Conclusion
Task 1 provided actionable insights into customer behavior and spending patterns.
Task 2 generated customer recommendations for personalized marketing.
Task 3 successfully segmented customers into clusters, aiding targeted business strategies.
This project delivers a comprehensive workflow for customer analytics, ensuring scalability and practical usability for businesses.
