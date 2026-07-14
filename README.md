# HepatoScreen ML: Classification and Clustering of Hepatitis C Laboratory Profiles

## Problem
Predict whether a laboratory record belongs to the healthy blood-donor group or the Hepatitis C/liver-disease group.

## Dataset
This project uses the UCI HCV dataset, which contains 615 observations and 12 clinical features.

## Methods
The project pipeline includes:
* **Missing-value imputation**: Handled using Category-specific mean imputation to prevent data leakage.
* **Standardization**: Feature scaling to ensure all laboratory markers contribute equally to model performance.
* **K-Nearest Neighbors (KNN)**: Implemented as a baseline distance-based classifier to evaluate local data structures..
* **Random Forest**: Used to capture non-linear relationships in laboratory data.
* **SVM**: Employed with an RBF kernel for classification.
* **Gradient Boosting**: Leveraged as an advanced boosting technique to sequentially minimize errors and maximize overall predictive performance.
* **PCA**: Applied for dimensionality reduction and 3D visualization of the data.
* **K-Means**: Used for unsupervised clustering to identify natural patient groupings.

## Supervised Learning Results

| Model | Disease Recall | Disease F1 | ROC-AUC |
| :--- | :--- | :--- | :--- |
| K Nearest Neighbours | 0.38 | 0.50 | 0.9097 |
| Support Vector Machine | 0.62 | 0.67 | 0.9699 |
| Random Forest | 0.50 | 0.67 | 0.9977 |
| Gradient Boosting | 0.88 | 0.93 | 0.9977 |

## Unsupervised Learning Results

### KMeans
| Disease/Cluster | 0 | 1 |
| :--- | :--- | :--- |
| 0 | 0.915371 | 0.084629 |
| 1 | 0.277778 | 0.722222 |

### PCA
2 components explained variance: 0.3890361591275746

3 components explained variance: 0.5132220171716534

## Limitations
* The sample is small. 
* The classes are imbalanced. 
* Multiple rows may not represent a broad population. 
* The model has not received clinical validation. 
* It must not be used for medical diagnosis.
