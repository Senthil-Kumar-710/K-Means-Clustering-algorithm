# Implementation of K-Means Clustering Algorithm


## Aim

To write a python program to implement K-Means Clustering Algorithm.

## Equipment’s required:

1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step 1

Import the necessary packages.

### Step 2

Read the csv file.

### Step 3

Scatter plot the applicant income and loan amount.

### Step 4

Obtain the kmean clustring for 2 classes.

### Step 5

Pretict the cluster group of Applicant Income and Loanamount.

## Program:
```
Developed By: Senthil Kumar S
Roll no: 212221230091

import pandas as pd
from sklearn.cluster import KMeans 
import matplotlib.pyplot as plt
import seaborn as sns 
x1 = pd.read_csv('clustering.csv') 
print (x1.head (2)) 
x2 = x1.loc[:,['ApplicantIncome', 'LoanAmount']] 
print(x2.head (2))
x=x2.values
sns.scatterplot (x[:,0],x[:,1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()
kmeans=KMeans(n_clusters=4)
kmeans.fit(x)
print("Cluster centers:", kmeans.cluster_centers_)
print("Labels:", kmeans.labels_)
predict_class = kmeans.predict([[9000, 1200]])
print("Cluster group for application income 9000 and loanamonunt 120 is",predict_class)
```
## Output:

![Capture](https://user-images.githubusercontent.com/93860256/154078476-1c69824c-6000-4503-8cb5-9989a6b2100c.PNG)


## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.