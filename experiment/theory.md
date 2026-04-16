
#### K-MEANS CLUSTERING 


##### OVERVIEW

K-Means Clustering is an unsupervised machine learning algorithm used to partition a dataset into a predefined number of clusters (K). The algorithm groups data points such that points within the same cluster are more similar to each other than to points in other clusters.

It operates iteratively by assigning data points to clusters and updating cluster centers until a stable structure is achieved.


#####  DATA REPRESENTATION

A dataset consists of multiple data points, where each data point is described by a set of features (attributes). These features define the position of each data point in a multi-dimensional space called the feature space.

The similarity between data points is determined using a distance measure. The most commonly used distance metric is Euclidean distance, which calculates how far apart two points are in the feature space.



#####  CLUSTER AND CENTROID CONCEPT

Cluster:
A cluster is a collection of data points grouped together based on similarity. Points in the same cluster are expected to be close to each other in the feature space.

Centroid:
A centroid is the representative point of a cluster. It is defined as the mean position of all data points assigned to that cluster. The centroid may not necessarily correspond to an actual data point.

The position of the centroid changes during the algorithm as cluster assignments are updated.



#####  OBJECTIVE OF THE ALGORITHM

The goal of K-Means is to create clusters that are as compact and distinct as possible. This means:
- Data points within a cluster should be close to their centroid.
- Different clusters should be well separated from each other.

The algorithm attempts to minimize the overall distance between data points and their respective cluster centroids.



#####  ALGORITHM WORKFLOW

Step 1: Initialization
The algorithm begins by selecting K initial centroids. These can be chosen randomly or using more advanced methods such as k-means++ to improve stability.

Step 2: Assignment Step
Each data point is assigned to the cluster whose centroid is closest. This step forms K clusters based on current centroid positions.

Step 3: Update Step
After assignment, each cluster’s centroid is recomputed as the mean of all data points assigned to that cluster. This shifts the centroid to a new position that better represents the cluster.

Step 4: Iterative Refinement
Steps 2 and 3 are repeated. With each iteration:
- Data points may change clusters
- Centroids move to new positions

This process continues until the clustering stabilizes.



#####  CONVERGENCE CRITERIA

The algorithm is considered to have converged when:
- The centroids no longer change significantly between iterations, or
- The assignment of data points to clusters remains unchanged

At convergence, the clusters are stable and further iterations do not improve the result.



#####  ROLE OF DISTANCE METRIC

The choice of distance metric directly affects clustering results.

Euclidean distance is most commonly used because:
- It measures straight-line distance in feature space
- It works well when clusters are spherical and evenly distributed

Other distance measures may be used depending on the nature of the data.


#####  IMPORTANCE OF FEATURE SCALING

K-Means is sensitive to the scale of features because distance calculations are affected by the magnitude of values.

If one feature has a much larger range than others, it will dominate the clustering process.

Standardization (Z-score normalization) is commonly applied to:
- Ensure all features contribute equally
- Improve clustering accuracy



#####  SELECTION OF K (NUMBER OF CLUSTERS)

The value of K must be specified before running the algorithm. Choosing an appropriate K is critical.

Elbow Method:
- Plot the clustering error against different values of K
- Identify the point where improvement slows down significantly
- This point is considered a good choice for K

Silhouette Score:
- Measures how well each data point fits within its cluster
- Higher values indicate better-defined clusters
- Can be used to compare different values of K



#####  PERFORMANCE CHARACTERISTICS

Advantages:
- Simple and easy to implement
- Efficient for large datasets
- Works well when clusters are well separated

Limitations:
- Requires prior knowledge of K
- Sensitive to initial centroid placement
- May converge to a local optimum instead of the global optimum
- Assumes clusters are spherical and similar in size
- Not suitable for clusters with irregular shapes or varying densities

