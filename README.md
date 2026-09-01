# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Start the program.

2.Import required libraries like pandas, matplotlib, and sklearn.

3.Load the Mall_Customers.csv dataset.

4.Select Annual Income and Spending Score as features.

5.Initialize an empty list to store WCSS values.

6.Apply K-Means for cluster values from 1 to 10.

7.Store inertia (WCSS) for each cluster value.

8.Plot the Elbow graph to find the optimal number of clusters.

9.Train K-Means again using the chosen number of clusters (e.g., 5).

10.Predict clusters, assign them to customers, and visualize the clusters using scatter plot.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Surya Prakash S
RegisterNumber: 212225040443
*/
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv(r"C:\Users\admin\Downloads\Mall_Customers (1).csv")
X = data.iloc[:, [3, 4]].values
kmeans = KMeans(n_clusters=5, random_state=0)
y_kmeans = kmeans.fit_predict(X)
plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=100)
plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")
+plt.show()
```

## Output:

<img width="772" height="510" alt="image" src="https://github.com/user-attachments/assets/6e77fa56-2dce-4bbb-a16a-fc14cf465e5c" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
