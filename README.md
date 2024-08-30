# Unsupervised-Learning

The objective of this assessment is to apply and evaluate clustering techniques using the Iris dataset, a well-known dataset in machine learning and statistics. The assessment involves loading and preprocessing the data, implementing KMeans and Hierarchical clustering algorithms, and visualizing the resulting clusters

Dataset
Dataset was directly imported from sklearn.datasets and implemented

Overview
The objective of this assessment is to apply and evaluate clustering techniques using the Iris dataset, a well-known dataset in machine learning and statistics. The assessment involves loading and preprocessing the data, implementing KMeans and Hierarchical clustering algorithms, and visualizing the resulting clusters.

Dataset Overview:
The Iris dataset is a well-known dataset that contains measurements of four features from three different species of Iris flowers.

![image](https://github.com/user-attachments/assets/61585758-f03e-4ae9-9cad-e68c248ba2f2)


The features are:

Sepal length

Sepal width

Petal length

Petal width

The dataset contains 150 samples with each sample belonging to one of three species: Iris setosa, Iris versicolor, and Iris virginica. For clustering purposes, the species column will be dropped to focus solely on the feature data.

Loading and Preprocessing
Load the Iris Dataset
Dataset was directly imported from sklearn.datasets and implemented in this project

Preprocessing Steps:
Drop the Species Column: Since the species label is not used in clustering, it will be excluded from the feature set. As this Dataset didn't have any target column, no need for dropping here

Finding the null values, Find the outliers in the dataset and finding the duplicated values.

Standardize the Data : Although not specified, it is often beneficial to scale the data to ensure that all features contribute equally to the clustering process.

Clustering Algorithm Implementation
A) KMeans Clustering
Description: KMeans clustering is an unsupervised learning algorithm that partitions the dataset into K distinct, non-overlapping subsets (clusters). It iteratively assigns data points to the nearest cluster center and updates the cluster centers by minimizing the variance within each cluster. The algorithm requires the number of clusters (K) to be specified beforehand.

Suitability for Iris Dataset: KMeans is suitable for the Iris dataset because it is efficient with small to medium-sized datasets and works well when clusters have a roughly spherical shape. The Iris dataset's features are numeric, and the clusters are relatively well-separated, making it a good candidate for KMeans.

Implementation:
Preprocessing: Standardize the features to have zero mean and unit variance using StandardScaler.

Clustering: Apply KMeans with K=3 (as the dataset has three species and confirmed by elbow method, domain knowledge and silhouette score method).

Visualization: Use a scatter plot to visualize the clusters, coloring points by the cluster labels assigned by the algorithm.

B) Hierarchical Clustering
Description: Hierarchical clustering is a technique that builds a hierarchy of clusters. It can be agglomerative (bottom-up) or divisive (top-down). Agglomerative clustering starts with each data point as a separate cluster and merges them iteratively until all points belong to a single cluster. The choice of linkage criterion (e.g., single, complete, average) affects how the distance between clusters is computed.

Suitability for Iris Dataset: Hierarchical clustering is useful for exploring data when the number of clusters is not known in advance. It provides a dendrogram, which is a tree-like diagram that shows the arrangement of the clusters formed at each stage. This can help identify the optimal number of clusters by examining where large jumps in distances occur.

Implementation:
Preprocessing: Use the same standardized data as in KMeans.

Clustering: Apply agglomerative hierarchical clustering with different linkage criteria (e.g., 'ward', 'complete'). No of clusters '3' found by plotting a dendogram

Visualization: Used a dendrogram to visualize the hierarchical structure and a scatter plot to visualize the final clusters.

Conclusion
After implementing and visualizing both clustering techniques, analyze the resulting clusters to evaluate their quality and interpretability. Discuss the insights gained from the clustering analysis and compare the results of KMeans and Hierarchical clustering.
