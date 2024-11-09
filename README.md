# CryptoClustering
# Cryptocurrency Clustering using K-means and PCA

## Overview

This project aims to cluster cryptocurrencies using K-means clustering. The analysis involves normalizing the data, determining the optimal number of clusters (k) using the elbow method, and optimizing the clustering process with Principal Component Analysis (PCA). The final results will be visualized through scatter plots to better understand the relationships between different cryptocurrencies.

## Instructions

### Step 1: Rename the Notebook
Rename the file `Crypto_Clustering_starter_code.ipynb` to `Crypto_Clustering.ipynb`.

### Step 2: Load the Data
- Load the `crypto_market_data.csv` into a Pandas DataFrame.
- Retrieve summary statistics and plot the data to visualize its structure before further analysis.

### Step 3: Prepare the Data
- Normalize the data using the `StandardScaler()` module from scikit-learn.
- Create a new DataFrame with the scaled data and set the `coin_id` index from the original DataFrame as the index for the new DataFrame.

### Step 4: Find the Best Value for k Using the Scaled DataFrame
Utilize the elbow method to determine the best value for k:
- Create a list of k values ranging from 1 to 11.
- Initialize an empty list to store inertia values.
- Implement a for loop to compute inertia for each k value.
- Create a dictionary to plot the elbow curve.
- Generate a line chart to visualize the inertia values and identify the optimal k.
- Document the best value for k in the notebook.

### Step 5: Cluster Cryptocurrencies with K-means Using the Scaled DataFrame
- Initialize the K-means model with the identified best value for k.
- Fit the K-means model using the scaled DataFrame.
- Predict clusters to group the cryptocurrencies and add a new column with the predicted clusters to a copy of the scaled DataFrame.
- Create a scatter plot using `hvPlot`:
  - Set the x-axis to `price_change_percentage_24h` and the y-axis to `price_change_percentage_7d`.
  - Color the points based on the K-means labels.
  - Include the `coin_id` column in the `hover_cols` parameter for identification.

### Step 6: Optimize Clusters with Principal Component Analysis (PCA)
- Perform PCA on the original scaled DataFrame to reduce features to three principal components.
- Retrieve and document the explained variance to assess the information captured by each component.
- Create a new DataFrame with the scaled PCA data, setting the `coin_id` index from the original DataFrame.

### Step 7: Find the Best Value for k Using the PCA DataFrame
Apply the elbow method on the scaled PCA DataFrame:
- Create a list of k values from 1 to 11.
- Initialize an empty list for inertia values.
- Implement a for loop to compute inertia for each k value.
- Create a dictionary to plot the elbow curve.
- Generate a line chart to visualize the inertia values and identify the optimal k.
- Document the best value for k found using the PCA DataFrame and compare it with the previous k value.

### Step 8: Cluster Cryptocurrencies with K-means Using the PCA DataFrame
- Initialize the K-means model with the best value for k from the PCA analysis.
- Fit the K-means model using the scaled PCA DataFrame.
- Predict clusters and add a new column to store the predicted clusters in a copy of the scaled PCA DataFrame.
- Create a scatter plot using `hvPlot`:
  - Set the x-axis to `PC1` and the y-axis to `PC2`.
  - Color the points based on the K-means labels.
  - Include the `coin_id` column in the `hover_cols` parameter for identification.
- Answer the question regarding the impact of using fewer features for clustering with K-means.

## Conclusion

This project provides a comprehensive approach to clustering cryptocurrencies using K-means and PCA. By following the outlined instructions, you will gain insights into the relationships between different cryptocurrencies and the effectiveness of clustering techniques in data analysis.
