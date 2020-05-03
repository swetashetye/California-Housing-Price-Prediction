This is a regression problem to predict California housing prices.
The dataset contains 20640 entries and 10 variables.
 Longitude
 Latitude
 Housing Median Age
 Total Rooms
 Total Bedrooms
 Population
 Households
 Median Income
 Median House Value
 Ocean Proximity
Median House Value is to be predicted in this problem.
I have done this project in two parts.
 First part contains data analysis and cleaning
 Second is training of machine learning models.
1) Analysis and Data Cleaning
I have done the data analysis and done following manipulations on data.
1. Loading the dataset
2. Extract Features(X) and Label(Y) data from the dataset.
List of Features(X): longitude, latitude, housing_median_age, total_rooms, total_bedrooms,
population, households, median_income, ocean_proximity
Label(Y): median_house_value
3. Handle missing values
Checked whether there are any missing values or null, and found that total_bedrooms
column has 207 null values. So I performed Imputation with mean strategy.
4. Encode categorical data
After analysing, found that one of the columns is a categorical feature (ocean_proximity). I
had to apply LabelEncoder to convert it into numerical data.
5. Split the dataset
Splited the data into 80% training dataset and 20% test dataset using train_test_split from
sklearn.model_selection lib.
6. Standardize data of training and test data.
It is a step of Data Pre Processing, the process of putting different variables on the same
scale.
2) Training machine learning algorithms:
Here, I have trained various machine learning algorithms and calculated Root Mean Squared
Error (RMSE)
 Linear Regression
RMSE : 71098.69982050032
 Decision Tree Regression
RMSE: 70879.2196382473
 Random Forest Regression
RMSE: 50681.311813414475
So it is observed that Random Forest Regression gives Lower values of RMSE which
indicates better fit.
Lastly Linear Regression with one independent variable
Perform Linear Regression to predict housing values based on independent variable:
median_income
Observation: The independent variable is scattered so that we are getting less accurate
results.
