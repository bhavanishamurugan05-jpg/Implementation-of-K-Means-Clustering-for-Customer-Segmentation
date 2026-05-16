# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load and preprocess the customer dataset by selecting relevant features.
2.Use the Elbow Method to determine the optimal number of clusters (K).
3.Apply the K-Means algorithm to group customers into clusters.
4.Visualize and analyze the clusters for customer segmentation.. 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: BHAVANISHA.M
RegisterNumber: 212225230034 
*/
```
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = pd.read_csv("Mall_Customer.csv")

X = data.iloc[:, [3, 4]].values

kmeans = KMeans(n_clusters=5, random_state=0)

y_kmeans = kmeans.fit_predict(X)

plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=50)
plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")
plt.show()
```
## Output:

<img width="916" height="562" alt="image" src="https://github.com/user-attachments/assets/7d2aabdf-68c3-4219-b350-bbfe7c01c72b" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
