# Zomato-Ratings-Deployment
Restaurant Rating Prediction & Deployment

Project Overview:

This project predicts restaurant ratings based on various factors such as online orders, table bookings, restaurant type, location, and cuisine. Machine learning models were trained and deployed using Flask to provide real-time predictions.

Datasets:
1- https://drive.google.com/file/d/1bmghmXygKsQNNYl_FR0CcdCeIGP2wagn/view?usp=drive_link (orignal zomato.csv file)
2- https://drive.google.com/file/d/1JZJfugs09VDbMuiMZ3on7W2MO55SbR6U/view?usp=drive_link (pickle file containing the extra-tree regressor Model)

Exploratory Data Analysis (EDA)
Dataset Overview: The dataset was checked for null values, duplicates, and data types.
Data Cleaning: Missing values were handled, and categorical variables were encoded.
Feature Engineering: New features such as cost normalization and restaurant categorization were created.

Data Engineering
Data Preprocessing:
Columns like cost and rate were converted to numeric values.
Unnecessary columns like phone and url were dropped.
Label encoding was applied to categorical variables such as location, rest_type, and cuisines.

After Data engineering and EDA a simple Numerical Dataset (Zomato_df.csv) is created
which is smaller in size and perfect for model prediction

Charts Used
Bar Charts: Used to visualize the most popular restaurants, top cuisines, and service types.
Count Plots: Showed the frequency of online orders and table bookings.
Pie Charts: Represented the proportion of restaurants by rating categories.
Box Plots: Displayed the distribution of restaurant costs.
Histograms: Illustrated rating distributions.

Outliers
Cost Outliers: High-end restaurants had extreme cost values.
Ratings Outliers: Ratings below 2 were rare, indicating a possible skew in the data.

Models Used
Linear Regression: Basic predictive model to estimate restaurant ratings. R2 score was very low(0.22)
Random Forest Regressor: Used for capturing complex relationships in the data. Good R2 score(0.88)
Extra Trees Regressor: Employed to improve model accuracy. best R2 score achieved (0.93)

After R² scores were computed to evaluate each model conclusion was made that Extra Tree Regressor will be used for creating the Pickle File

How to use the Deployment file

1- Download all the files from the project 
2- keep all the files in the same directory
3- if any further tweaking is required by the end user they can download the large dataet from google drive link given in readdme
4- Run Model.py file in an ide
5- Run app.py , open the link given in the terminal 
6- Enter the values and click predict

File Descriptions:
Model.py:
This file contains the code for building the model that is used in predicting the restaurant ratings
end user can run ipynb file and create a new pickle file and make changes to model.py.

csv file:
This contains our data that wws cleaned and saved (contains encoded/numerical data) after data engineering

template file:
The template file contains the html and css documents used in building the web app

App.py:
This contains the Flask API’s that receives restaurant details via a GUI/API calls, then make the prediction of restaurant ratings based on the model and returns the rate









