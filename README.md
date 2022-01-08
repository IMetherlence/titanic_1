# Kaggles Titanic Project

This project aims to apply Supervised Machine Learning process onto our Titanic dataset.

---

## Data Cleaning:

Column names are standardized to lower case without spaces.  

`passengerid` is then set as the index column of both test and train datasets  

Age data with missing values are imputed with the mean of the data instead.

Names have their special characters removed.

`ticket` column is removed due to having excess missing data

`sex` column is binary encoded.

`embarked` column is categorically encoded.

---

## Exploratory Data Analysis

Heatmap of our train dataset is made to explore multicollinear variables, in which none were found to be above threshold of +-0.7.  
There is not many highly correlated data in our target variables, aside from the `sex` column.  
A pairplot is afterwards made to explore our other variables.  

---

## Modelling
Manual modelling was ran into a function to evaluate our data directly, in which it yielded a low R2 score, indicating that either there is insufficient correlated data, or there is the presence of noise and outliers in the dataset. 

Afterwards, PyCaret was used to run different models to verify our model with appropriate hyperparameters. The best 3-5 models were chosen to be the deployed models and used to generate a prediction which will be used for our submissions.