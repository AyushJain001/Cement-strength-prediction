# Cement-strength-prediction

**Problem Statement**
-To build a regression model to predict the concrete compressive strength based on the different features in the training data. 

*Architecture*


![Data Processing Steps](https://user-images.githubusercontent.com/90152799/185467421-c90e526f-eeeb-4e49-8383-b4efb5eaa68e.jpg)





*Result-*


Model performed well with accuracy greater than 85%.

How to Run:


1-git init


2-git add .


3-git commit -m "Initial commit"


4-git remote add origin remoteurl



5-git push origin master/ git push -f origin master

*Prediction*
 
1) Data Export from Db - The data in the stored database is exported as a CSV file to be used for prediction.
2) Data Preprocessing   
   a) Check for null values in the columns. If present, impute the null values using the KNN imputer
   b) transform the features using log transformation
   c) Scale the training and test data separately 
3) Clustering - KMeans model created during training is loaded, and clusters for the preprocessed prediction data is predicted.
4) Prediction - Based on the cluster number, the respective model is loaded and is used to predict the data for that cluster.
5) Once the prediction is made for all the clusters, the predictions along with the original names before label encoder are saved in a CSV file at a given location and the location is returned to the client.




Dashboard Overview-


<img width="923" alt="image" src="https://user-images.githubusercontent.com/90152799/180617470-107ab536-9024-4dbd-a683-83f6e4ef971c.png">
