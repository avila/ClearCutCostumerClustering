# Challenge Description

## Project: Customer Segmentation for Supermarkets

---

## Task

You are provided with a dataset of supermarket customer data. The goal
is to perform clustering analysis to segment customers based on their
demographic, spending behavior, and other features. This will help
identify customer groups for targeted marketing strategies.

Your task is to build an unsupervised learning model to cluster
customers effectively. After identifying clusters, describe the
characteristics of each group and provide insights into potential
business strategies.

---

## File Description

\- **Supermarket\_customers.csv**: The dataset containing
demographic and behavioral data of supermarket customers. Key features
include:

\- CustomerID: Unique ID for each customer.  
- Gender: Male or Female.  
- Age: Customer's age.  
- Annual\_Income: Annual income of the customer in thousands.  
- Spending\_Score: A score assigned by the supermarket based on customer
behavior and loyalty.

## Submission File

For each customer, you must assign a cluster label (e.g., Cluster 1,
Cluster 2, etc.). The submission file should contain a header and be in
the following format:

CustomerID,Cluster  
1,Cluster\_1  
2,Cluster\_3  
3,Cluster\_2  
  
Where:  
- **CustomerID** corresponds to the unique customer ID from the
dataset.  
- **Cluster** is the label of the assigned cluster.

## Evaluation Metric

Your solution will be evaluated on the following:  
1. **Clustering Validity**: Use metrics like silhouette score or
Davies-Bouldin index to justify your clusters.  
2. **Business Insights**: Provide a well-explained analysis of each
cluster and potential marketing strategies.


