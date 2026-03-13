

### 1. Introduction to K-Means Clustering

**K-Means Clustering**: An "unsupervised" machine learning algorithm. Its job is to automatically find hidden patterns in data by grouping similar items together into a specific number of groups (called K). "Unsupervised" means we don't tell the algorithm what the groups are in advance; it figures it out on its own.

**Dataset**: The collection of data we are analyzing. In this simulation, it's a famous dataset of different wines.

**Features**: The specific, measurable properties of the data. For the wines, features include things like Alcohol content, Malic Acid, or Color Intensity. On the scatter plot, you pick two features to represent the X-axis and Y-axis.

### 2. The Anatomy of a Cluster

**Cluster**: A group of data points that are mathematically similar to each other. In the app, points in the same cluster share the same color.

**Centroid**: The "center of gravity" or the average position of a cluster. It is represented by the large, bold crosshair (+) on the scatter plot. The algorithm's entire goal is to find the perfect resting place for these centroids.

**K**: The mathematical symbol for the number of clusters (and centroids) you want the algorithm to find. If K=3, the algorithm will hunt for 3 distinct groups.

### 3. The Algorithm's Process

**Initialization**: The very first step where the starting centroids are dropped onto the graph. This can be done randomly by the computer, or manually by you clicking on the graph.

**Point Assignment**: The step where the algorithm measures the distance from every single data point to every centroid. Each point is then "assigned" to the centroid it is closest to.

**Centroid Update**: Once points are assigned, the old centroid is deleted and a new centroid is calculated by finding the exact geographic center (the average/mean) of all the points in that newly formed group.

**Iteration**: One complete cycle of Point Assignment followed by Centroid Update.

**Convergence**: The finish line. Convergence happens when the centroids stop moving. If you run an iteration and no data points switch to a different cluster, the algorithm has "converged" and the simulation is complete.

### 4. Measuring Success & Tuning

**Standardization (Z-Score)**: A preprocessing step. Some wine features have naturally huge numbers (like Proline, which goes up to 1500), while others are tiny (like Hue, which is around 1.0). If you don't standardize, the algorithm will only care about the huge numbers. Standardization shrinks and stretches the data so every feature is measured on the exact same scale.

**WCSS (Within-Cluster Sum of Squares)**: A math formula that measures how "tight" or compact the clusters are. A lower WCSS means the data points are huddled very closely around their centroid.

**The Elbow Method**: A visual trick to help you guess the best number for K. You look at a line graph of the WCSS. As you add more clusters, the WCSS drops. The "elbow" is the point on the graph where the line stops dropping steeply and starts to flatten out. That elbow is usually the optimal K.

**Silhouette Score**: A final grade for your clustering, ranging from -1 to 1.
- Near 1: Excellent. Clusters are tight and far away from other clusters.
- Near 0: Overlapping. Clusters are bleeding into one another.
- Near -1: Terrible. Data points were likely assigned to the wrong clusters.