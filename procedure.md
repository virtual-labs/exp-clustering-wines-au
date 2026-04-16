
 click the  **"Start Simulation"** button to begin.


#### Step 1: Data Preprocessing

<img src="images/step2.png" alt="Data Preprocessing" width="600"/>

Toggle the **"Standardize Features (Z-Score)"** switch on or off.

Turning it on ensures that features with larger numbers don't unfairly dominate the clustering process.

Click **"Next Step"**.



#### Step 2: Determine K (Number of Clusters)

<img src="images/step3.png" alt="Elbow Method Plot" width="600"/>

Look at the **"Elbow Method"** plot on the right.

Try to find the **"elbow" point** where the line starts to flatten out.

Use the **"Number of Clusters (K)"** slider on the left to set your desired number of clusters.

Click **"Next Step"**.



#### Step 3: Centroid Initialization

<img src="images/step5.png" alt="Centroid Initialization" width="600"/>

Choose your initialization method: **Random** or **Manual**.

If you chose **Random**:  
Click the **"Initialize Randomly"** button to let the app place the starting points.

If you chose **Manual**:  
Click directly on the **scatter plot** on the right to place your starting centroids yourself (**you must click exactly K times**).

Once the centroids are placed, click **"Next Step"**.



#### Step 4: Point Assignment

<img src="images/step6.png" alt="Point Assignment" width="600"/>

Click the  **"Calculate Assignments"** button.

You will see the data points change color to match their **closest centroid**.

Click **"Next Step"**.



#### Step 5: Centroid Update

<img src="images/step7.png" alt="Centroid Update" width="600"/>

Click the **"Move Centroids"** button.

Watch the larger centroid markers move to the **exact center of their newly assigned colored points**.

Click **"Next Step"**.



#### Step 6: Iterate

<img src="images/step8.png" alt="Iteration Process" width="600"/>

Click the  **"Auto-Iterate to Convergence"** button.

The app will automatically repeat the **assignment and update steps** until the centroids stop moving.

Wait a few seconds for it to finish.



#### Step 7: Results

<img src="images/step9.png" alt="Final Clustering Results" width="600"/>

Review your **final clusters**, the **total number of iterations**, and the **Silhouette Score** (which grades how well-separated your clusters are).

To try again with different features or a different **K**, click **"Reset Simulation"** at the bottom to start over.