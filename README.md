# CryptoClustering
Data Preprocessing

Standard Scaling: The data is normalized using the StandardScaler() module from scikit-learn to ensure consistent scaling across all features.

Creating Scaled DataFrame: A DataFrame with the scaled data is created, and the "coin_id" column is set as the index.

Finding the Best Value for k Using Original Scaled Data

To determine the optimal number of clusters using the elbow method, the following steps are taken:
Creating k-values List: A list is generated, ranging from 1 to 11, to represent the number of clusters.

Inertia Calculation: An empty list is created to store the inertia values. In a loop, the inertia values for each possible value of k are computed and appended to the list.

Elbow Curve: A dictionary is formed with the k-values and corresponding inertia values to plot an elbow curve. This helps in identifying the optimal value for k.

Optimal k: The optimal value for k is identified visually from the elbow curve, which represents the point where adding more clusters provides diminishing returns.

Clustering Cryptocurrencies with K-Means Using Original Scaled Data

For clustering cryptocurrencies using the original scaled data with the best value of k:

Initialize K-Means: The K-Means model is initialized using the previously determined optimal k.

Model Fitting: The K-Means model is fit to the original scaled DataFrame.

Predict Clusters: The clusters are predicted for each cryptocurrency, and these predictions are used to group the data.

Visualize Clusters: A copy of the original data is created, and a new column is added to store the predicted clusters. A scatter plot using hvPlot is generated, where "PC1" and "PC2" are set as the axes, and points are color-coded based on the clusters. The "coin_id" is included in the hover information to identify each cryptocurrency.

Dimensionality Reduction with PCA
Principal Component Analysis (PCA) is applied to reduce the features to three principal components, providing an alternative view of the data:

PCA Transformation: The original scaled data is used for PCA transformation.

Explained Variance: The explained variance is calculated to assess the information retained by each principal component.

New DataFrame: A new DataFrame is created with the PCA data, and the "coin_id" column is set as the index.


Sure, here's a README based on the tasks you performed:

README: Cryptocurrency Clustering with K-Means and PCA
This README outlines the steps taken to cluster cryptocurrencies using K-Means and Principal Component Analysis (PCA). The process involves data preprocessing, identifying optimal cluster counts, clustering using both the original scaled data and PCA data, and analyzing the impact of dimensionality reduction on the clustering results.

Data Preprocessing
Standard Scaling: The data is normalized using the StandardScaler() module from scikit-learn to ensure consistent scaling across all features.

Creating Scaled DataFrame: A DataFrame with the scaled data is created, and the "coin_id" column is set as the index.

Finding the Best Value for k Using Original Scaled Data
To determine the optimal number of clusters using the elbow method, the following steps are taken:

Creating k-values List: A list is generated, ranging from 1 to 11, to represent the number of clusters.

Inertia Calculation: An empty list is created to store the inertia values. In a loop, the inertia values for each possible value of k are computed and appended to the list.

Elbow Curve: A dictionary is formed with the k-values and corresponding inertia values to plot an elbow curve. This helps in identifying the optimal value for k.

Optimal k: The optimal value for k is identified visually from the elbow curve, which represents the point where adding more clusters provides diminishing returns.

Clustering Cryptocurrencies with K-Means Using Original Scaled Data
For clustering cryptocurrencies using the original scaled data with the best value of k:

Initialize K-Means: The K-Means model is initialized using the previously determined optimal k.

Model Fitting: The K-Means model is fit to the original scaled DataFrame.

Predict Clusters: The clusters are predicted for each cryptocurrency, and these predictions are used to group the data.

Visualize Clusters: A copy of the original data is created, and a new column is added to store the predicted clusters. A scatter plot using hvPlot is generated, where "PC1" and "PC2" are set as the axes, and points are color-coded based on the clusters. The "coin_id" is included in the hover information to identify each cryptocurrency.

Dimensionality Reduction with PCA
Principal Component Analysis (PCA) is applied to reduce the features to three principal components, providing an alternative view of the data:

PCA Transformation: The original scaled data is used for PCA transformation.

Explained Variance: The explained variance is calculated to assess the information retained by each principal component.

New DataFrame: A new DataFrame is created with the PCA data, and the "coin_id" column is set as the index.

Finding the Best Value for k Using PCA Data
The optimal value for k is identified using PCA data by following the elbow method:

Creating k-values List: A list with k-values ranging from 1 to 11 is generated.

Inertia Calculation: Inertia values are calculated for each k value, and the results are used to create an elbow curve.

Optimal k for PCA: The elbow curve is used to identify the optimal k for PCA data, which may differ from the best k value obtained using the original data.

Clustering Cryptocurrencies with K-Means Using PCA Data
To cluster cryptocurrencies using PCA data with the optimal k:

Initialize K-Means: The K-Means model is initialized with the optimal k value determined for PCA.

Model Fitting: The K-Means model is fitted to the PCA data.

Predict Clusters: Predictions are made for the clusters, and a new column is added to a copy of the PCA data DataFrame to store the predicted clusters.

Visualize Clusters: A scatter plot using hvPlot is generated with "price_change_percentage_24h" and "price_change_percentage_7d" as axes. Points are color-coded based on the clusters, and the "coin_id" is included in the hover information to identify each cryptocurrency.

Analyzing the Impact of Dimensionality Reduction
The final question to address is the impact of using fewer features (principal components) for clustering data using K-Means. This can be explored by comparing the results obtained from the original scaled data and the PCA data, and how it affects the interpretation of clusters.
