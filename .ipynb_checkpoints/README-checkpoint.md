[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/1YFwPRoH)
# Vertebral Column Classification (Homework 1)

## Overview
This project implements **k-Nearest Neighbors (KNN)** classification on the [UCI Vertebral Column Dataset].  
The dataset is provided in two versions:
- **2C dataset** (`column_2C.dat`): Binary classification (Normal vs. Abnormal).  
- **3C dataset** (`column_3C.dat`): Multiclass classification (Normal, Disk Hernia, Spondylolisthesis).

The assignment includes:
1. **Data download and preprocessing**  
   - Download dataset from UCI (zip file).  
   - Read `.dat` files into pandas DataFrames.  
   - Add column names and encode class labels.  

2. **Exploratory Data Analysis (EDA)**  
   - Scatterplot matrix of features with class coloring.  
   - Boxplots of each feature by class.  

3. **Train/Test Split**  
   - Use first 70 rows of Class 0 and first 140 rows of Class 1 as **training set**.  
   - Remaining samples form the **test set**.  

4. **KNN Classification (Euclidean distance)**  
   - Evaluate train/test errors for different values of k (e.g., {208, 205, …, 7, 4, 1}).  
   - Select the optimal k (`k*`).  
   - At `k*` and `k*/2`, compute:
     - Confusion Matrix  
     - True Positive Rate (TPR)  
     - True Negative Rate (TNR)  
     - Precision  
     - F1-score  

5. **Learning Curve**  
   - Vary training set size N ∈ {10, 20, …, 210}.  
   - For each N, select best k from {1, 6, 11, …}.  
   - Plot best test error rate vs training set size.  

6. **Other Distance Metrics**  
   - Manhattan (p=1)  
   - Minkowski with log10(p) ∈ {0.1, …, 1}  
   - Chebyshev (p→∞)  
   - Mahalanobis (with covariance matrix inverse)  
   - Summarize best test errors in a table.  

7. **Weighted Voting**  
   - Replace majority polling with distance-weighted voting.  
   - Compare Euclidean, Manhattan, Chebyshev distances.  

8. **Lowest Training Error**  
   - Report the lowest training error rate achieved across all experiments.  
   - Include Leave-One-Out (LOO) training error for fairer evaluation.