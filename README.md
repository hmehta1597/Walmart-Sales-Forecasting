# Walmart-Sales-Forecasting

Accurate sales forecasting is essential for businesses to optimize their inventory, project revenue, and inform investment decisions. For a large company like Walmart, understanding seasonal variations in sales is particularly critical. The objective of this project is to develop a model that can accurately forecast weekly sales, considering factors such as seasonality, holidays, promotional events, and economic conditions.

**Data Description**
The dataset used for this project is sourced from Kaggle and is divided into four subsets:

1)Features Dataset: Includes data such as temperature, fuel price, promotional markdowns, CPI (Consumer Price Index), and unemployment rates. These variables are recorded weekly and are specific to each store and date.

2)Stores Dataset: Provides fundamental information about each Walmart store, including the type of store and its size.

3)Train Dataset: Contains historical sales data for 98 products across 45 Walmart stores covering dates from 2010 to 2012.

4)Test Dataset: Mirrors the structure of the Train dataset but without the weekly sales figures which are to be predicted.

**Data Cleaning & Exploratory Data Analysis**

Data Cleaning

1)Handled missing values in the markdown columns of the Features dataset by converting 'NA' string values to nulls.

2)Converted economic indicators such as CPI and unemployment rate to numeric data types.

Exploratory Data Analysis

1)Aggregated store size data to find the minimum, average, and maximum store sizes for each type.

2)Constructed a time series plot depicting weekly sales from February 2010 to October 2012.

3)Analyzed temperature trends across different types of Walmart stores.

4)Investigated the impact of fuel prices on sales, concluding that temperature and fuel price changes do not significantly affect sales.

**Modeling Techniques**

Decision Tree: A tree-based model that partitions the data based on feature values.

Random Forest: An ensemble learning technique that constructs multiple decision trees on different subsets of the data.

XGBoost: An advanced implementation of gradient boosting, highly efficient, and flexible with built-in regularization to prevent overfitting.

**Results**

Decision Tree Model
Accuracy: 87.81%
RMSE (Training): 7662.26
R-squared (Training): 0.8800
RMSE (Testing): 7744.60
R-squared (Testing): 0.8782

Random Forest Model
Accuracy: 98.021%
RMSE: 3121.822
R-squared: 0.98021

XGBoost Model
Accuracy: 98.348%
RMSE: 2852.098
R-squared: 0.98348

The XGBoost model outperformed the other two models, achieving the highest accuracy and lowest RMSE.
