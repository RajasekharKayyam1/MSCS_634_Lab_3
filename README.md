# MSCS 634 – Lab 3: K-Means vs. K-Medoids Clustering

**Student:** Rajasekhar Reddy Kayyam  
**Course:** MSCS 634 – Advanced Big Data & Data Mining

## Purpose
Cluster the scikit-learn Wine Dataset using K-Means and K-Medoids (PAM), both with k=3, and compare Silhouette Scores, Adjusted Rand Indices, and PCA scatter plots.

## Method
- Explore 178 records, 13 features, and 3 actual classes.
- Standardize features using z-score normalization (`StandardScaler`).
- Fit K-Means and a self-contained NumPy implementation of K-Medoids (PAM) with multiple seeded starts.
- Evaluate clustering in all 13 dimensions, then project to 2D with PCA for visualization.
- Reference class labels are **not** used to train either clustering algorithm.

## Key insights
After running the notebook, use the displayed comparison table to identify which algorithm has the higher Silhouette Score (cluster definition) and ARI (agreement with actual classes). These two metrics measure different qualities. The side-by-side plot shows differences in cluster positions and their representative centroids/medoids.

## Challenges and decisions
Wine features have different scales, so standardization is necessary. K-Medoids is implemented using NumPy instead of `scikit-learn-extra` to avoid binary compatibility problems. PAM is more computationally expensive than K-Means; multiple starts improve reliability. PCA is used only for visualization, not to compute the clustering metrics.

## How to run locally
1. Extract the ZIP and open CMD inside the `MSCS_634_Lab_3` folder.
2. Run `python -m pip install -r requirements.txt`.
3. Run `jupyter notebook MSCS_634_Lab_3.ipynb`.
4. In the browser, choose **Run → Run All Cells** and save with **Ctrl+S**.
5. The notebook creates `clustering_comparison.png`. Commit the executed notebook, plot, README, and requirements file to your public GitHub repository.

## Submission
Submit your public GitHub repository URL in Blackboard.
"# MSCS_634_Lab_3" 
