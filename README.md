# CryptoClustering
This project utilizes the k-means algorithm and SciKitLearn to cluster data relating to cryptocurrency.

Data is prepared using "StandardScaler()" (documentation: https://scikit-learn.org/stable/auto_examples/preprocessing/plot_all_scaling.html#standardscaler) which scales the data according to variance. This scaling reduces the scope of range of the dataset.

K-means clustering is used to analyze the scaled data by plotted distance, grouping them into clusters of similar data points.
 "K", or number of clusters, must be determined to maximally utilize K-means for clustering.
 
With the scaled data, the "elbow method" is used to determine the best "k" value. 
The elbow method tests a differing number of cluster centers, taking the sum-of-square distance for points from each cluster center. When these values begin to diminish in change between each higher cluster number, functionality change in a higher k value becomes diminished. This is represented with an "Elbow Graph" visually, where the ideal k value is located where reduction of sum of square per cluster begins to drop off, or the "Elbow" of the graphed curve. 
(additional info source: https://builtin.com/data-science/elbow-method)
For this dataset, a k value of 4 is chosen.

Principal Component Analysis, or PCA for short, reduces dimensionality of the data. This may lead to more desireable grouping. In this case, the data is reduced to 3 principal components.
(additional info source: https://365datascience.com/tutorials/python-tutorials/principal-components-analysis/)

Upon comparison, although original complexity is lost, the resulting cluster plots for the original and PCA data show slightly better clustering with the use of PCA.
