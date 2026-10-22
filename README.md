# K-Means Clustering from Scratch in R

STAT 302 final project (Fall 2025), University of Washington.

## Overview
This project implements k-means clustering from scratch in base R, without the built-in `kmeans()` function, and uses the within-cluster sum of squares (WSS) to choose the number of clusters.

## Data
- Mall Customers dataset (200 customers), using the quantitative variables Age, Annual Income (k$), and Spending Score (1-100)
- Provided through course Canvas and also widely available on Kaggle. The data file is not included.

## Methods
- Random centroid initialization, distance calculation, cluster assignment, and centroid updates repeated until convergence
- WSS computed for k = 1 to 15, with the elbow plot used to choose k
- Clusters described using the clustering variables plus Gender
- Simulation study with three multivariate normal datasets (clear, weak, and no cluster structure) to test how k-means behaves
- Stability analysis: 10 random seeds, with the proportion of runs in which each pair of points lands in the same cluster

## Key Findings
- The WSS elbow on the Mall Customers data suggested k = 5.
- WSS dropped sharply and then flattened at k = 3 for the clearly clustered simulation and at k = 2-3 for the weakly clustered one. The no-cluster data showed a gradual decline with no clear elbow.
- Mean pairwise stability was similar across scenarios (about 0.33 to 0.35 at k = 3), so the average alone does not distinguish them.

## Files
- `302_FinalProject.pdf`: code and report

## Author
Zayna Badr, University of Washington
