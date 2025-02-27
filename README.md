# Project Report: Fashion MNIST Clustering using K-Means and PCA

This report outlines the steps taken and results achieved while working on clustering the Fashion MNIST dataset using K-Means and PCA for dimensionality reduction.

### 1. Dataset Overview

The dataset consists of images of fashion items (e.g., shoes, shirts, trousers, etc.), with each image being 28x28 pixels and represented as a vector of 784 features. The dataset is divided into two parts:

Training Data: 60,000 images.

Test Data: 10,000 images.

Each image is labeled with one of 10 categories (e.g., T-shirt, Sneaker, etc.).

### 2. Data Preprocessing
Data Loading: The dataset was loaded using pandas' read_csv function.

Data Normalization: All pixel values were scaled between 0 and 1 by dividing by 255.

Label Separation: The labels (fashion item categories) were separated from the pixel data for both training and test sets.

### 3. Dimensionality Reduction using PCA

Principal Component Analysis (PCA) was applied to reduce the feature space from 784 dimensions to 150 dimensions. This step was done to improve the performance of the clustering algorithm and reduce computational complexity.

### 4. Clustering with K-Means

K-Means Algorithm was applied to the reduced feature set.

Number of Clusters: 10 (corresponding to the 10 fashion categories).

The model was trained on the training data and used to predict cluster labels for the test data.

### 5. Evaluation Metrics

To evaluate the clustering performance, two metrics were used:

Silhouette Score: Measures how well-separated the clusters are. Higher values indicate better-defined clusters.

Silhouette Score: 0.17 (This indicates that the clustering model's separation of the data is not very strong and may need further improvement.)

Adjusted Rand Index (ARI): Measures the similarity between the predicted clusters and the actual labels.

ARI: 0.36 (This suggests a moderate alignment between the clustering results and the true labels, but still shows room for improvement.)

### 6. Visualizing the Clusters

To provide a better understanding of the clustering results, the following steps were taken:

Cluster Images: For each cluster, a representative image was displayed.

Confusion Matrix: A confusion matrix was generated to visually represent the performance of the clustering algorithm by comparing the predicted cluster labels with the true labels.

### 7. Results Summary
The Silhouette Score (0.17) indicates that the clusters are not well-separated, suggesting that the K-Means model is struggling to create meaningful groups.
The ARI Score (0.36) indicates that there is a moderate match between the predicted clusters and the actual labels, but it also shows that there is considerable room for improvement in the clustering quality.
Overall, the K-Means clustering using PCA on the Fashion MNIST dataset has shown moderate results. Further improvements could be made by experimenting with different clustering algorithms or reducing the dimensionality further.
### 8. Future Work
Hyperparameter Tuning: Fine-tuning the number of clusters or other parameters for the K-Means algorithm might improve results.

Other Clustering Algorithms: Exploring other clustering methods, such as Gaussian Mixture Models (GMM) or DBSCAN, could yield better results.

Dimensionality Reduction Techniques: Experimenting with other dimensionality reduction techniques like t-SNE or UMAP could lead to better clustering performance.
