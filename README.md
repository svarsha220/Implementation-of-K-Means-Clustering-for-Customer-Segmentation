# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1. Start the program

Step 2. Import the necessary python libraries

Step 3. Read the dataset of Mall_Customers csv file

Step 4. From sklearn libraary select the cluster and import KMeans Clustering

Step 5. Find the sum of squared distance between each points and the centroid in a cluster using Elbow Method

Step 6. Plot the graph x and y as Number of Clusters and wcss respectively

Step 7. Using the matplotlib library draw the scatter plot for the given number of clusters (ie. here n_clusters = 5)

Step 8. Stop the program
## Program:
```

/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: VARSHA S
RegisterNumber:  212222220055

import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv('Mall_customers.csv')
data.head()

data.info()

data.isnull()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss=[]

for i in range(1,11):
    kmeans=KMeans(n_clusters =i,init ="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)


plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km =KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])

y_pred =km.predict(data.iloc[:,3:])
y_pred

data["cluster"]=y_pred

df0=data[data["cluster"]==0]

df1=data[data["cluster"]==1]

df2=data[data["cluster"]==2]

df3=data[data["cluster"]==3]

df4=data[data["cluster"]==4]

df0.head()

df1.head()

df2.head()

df3.head()

df4.head()

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="blue",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="green",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="black",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
*/
```

## Output:

## DATA.HEAD():
   
![Screenshot 2024-10-29 151337](https://github.com/user-attachments/assets/79ae05b9-4e89-4432-8aee-0480c4ada305)

## DATA.INFO():

![Screenshot 2024-10-29 151344](https://github.com/user-attachments/assets/72310976-385f-4274-9769-41f7fda00f45)

## DATA.ISNULL().SUM():

![Screenshot 2024-10-29 151350](https://github.com/user-attachments/assets/59d1c97c-16c0-4ec6-bc49-f7335a7cc024)

## PLOT USING ELBOW METHOD:

![Screenshot 2024-10-29 151401](https://github.com/user-attachments/assets/9ccdd792-f8a5-4f19-90e4-58dfc0bc1c11)

## K-MEANS CLUSTERING:   

![Screenshot 2024-10-29 151409](https://github.com/user-attachments/assets/9b9814b9-7545-4f31-84ca-7955ac821490)

## Y-PRED ARRAY:

![Screenshot 2024-10-29 151417](https://github.com/user-attachments/assets/8037e225-4be5-4cc7-8f27-607efe8fad0e)

## CUSTOMER SEGMENT:

![Screenshot 2024-10-29 151425](https://github.com/user-attachments/assets/f9ceae72-62ec-4ff3-9b25-531f030dc6a3)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
