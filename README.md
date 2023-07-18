# fraud_analysis
CAPSTONE PROJECT - 1
FRAUD ANALYSIS USING ML ALGORITHMS

Problem Statement: In this capstone project, you are going to analyze customer’s purchase data set and build a machine learning algorithm to detect fraud purchases. And also you are going to perform customer segmentation

Dataset: Purchase_Fraud_Data.csv

Dataset Description: Every row in this dataset contains information about purchases from multiple customers. Along with purchase details, we also have customer basic details like gender, date of birth etc. Individual column description as follows

User_id: Customer unique id
Signup_time: Date & Time at which the customer signup in the platform
Purchase_time: The latest purchase date & time from a customer
Purchase_value: Total purchase amount
Device_id: Unique device ID from which purchase was done
Source: Medium through which customers reached the platform
Browser: Browser used while purchasing
IP_address: IP Address from which purchase was done
Class: 1 = Target class; Fraud transaction; 0=Regular transaction
Category: Type of product purchased
Dob: Date of birth of the customer

Exploratory Data Analysis

1.	Summarize numerical, categorical and date columns separately and list down your inferences
2.	Identify and perform missing value treatment using appropriate techniques
3.	Univariate analysis: For each column perform appropriate univariate analysis. (i.e. perform distribution analysis on numerical columns and frequency analysis on categorical columns)
4.	Multivariate analysis: Take combinations of multiple columns and identify the relationship between them.
a.	Categorical vs numerical columns – bar charts, boxplots
b.	Numerical vs numerical columns – scatter plot
c.	Categorical vs multiple numerical columns – scatter plot
d.	Correlation matrix
e.	…
5.	Perform statistical hypothesis test to identify the relationship between input and target variables

Base Model for Benchmark

1.	Convert all the input columns to numerical columns using one hot encoding
2.	Make sure you temporarily ignore the date columns and id columns
3.	Split the data in training and testing
4.	Build a simple decision tree with max_depth=5 and identify accuracy and f1 score. Keep this as a bench mark values to explain the improvement post feature engineering 

Feature Engineering

Using the original data, perform the following feature engineering techniques to create new columns for modelling
1.	Using all the date columns, extract the following information wherever necessary
a.	Year, month, day, hour, day of the week (mon, tue, etc)
2.	Using date of birth column, try to calculate the appropriate age of the customer. (Compute difference between purchase date and date of birth)
3.	Using age column, identify age buckets using binning method
4.	Compute no. of hours/days between purchase time and signup time
5.	For all appropriate numerical variables, compute buckets using binning method

Model Building

1.	Convert all the input variables to numeric
2.	Split the new data in to training and testing
3.	Build the following classification models using new data
a.	Decision Trees
b.	Random Forest
c.	Boosting techniques
d.	XGBoost
4.	For all the above classifiers, make sure that you perform hyper parameter tuning to select optimal value hyper parameters
5.	For all the above methods, report accuracy and f1 score
6.	Also in a single plot, compare the ROC curves for all the above models
7.	Choose an appropriate model based on above inferences and report the same

Customer Segmentation

The company would like to segment their customers using various attributes, so that they can perform targeted marketing campaign. Do the following to group the customers in the different clusters

1.	 In the original feature engineered dataset, exclude the following columns: ids, dates, class (target column)
2.	Convert all the input variables to numeric
3.	Using Elbow method identify optimal number of clusters required to group customers in to various clusters
4.	Perform K-Means clustering using appropriate number of clusters
5.	Tag each customer with a cluster
6.	Cluster-wise report average values of all input variables

