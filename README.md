# Sales Prediction Project.
## Analyzing Sales Drivers for Food Items,Predicting Sales Across Stores to Enhance Strategies
Author:Dina Al Botmeh
## The goal is to assist retailers in understanding the key properties of products and outlets that significantly impact sales. This project focuses on predicting sales for food items across various stores, enabling retailers to make data-driven decisions that enhance their sales strategies.
#Data Source:
Big Mart Sales Prediction:https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view
For this dataset, there were 8522 rows and 12 columns.
# Data Dictionary
| Variable Name         | Description                                                                         |
|-----------------------|-------------------------------------------------------------------------------------|
| Item_Identifier       | Product ID                                                                         |
| Item_Weight           | Weight of product                                                                   |
| Item_Fat_Content      | Low-fat or regular                                                                  |
| Item_Visibility       | Display area percentage allocated to the product                                    |
| Item_Type             | Product category                                                                    |
| Item_MRP              | Maximum Retail Price of the product                                                |
| Outlet_Identifier     | Store ID                                                                           |
| Outlet_Establishment   | Year the store was established                                                       |
| Outlet_Size           | Ground area covered by the store                                                    |
| Outlet_Location_Type  | Area type where the store is located                                               |
| Outlet_Type           | Grocery store or supermarket                                                        |
| Item_Outlet_Sales     | Sales of the product in the store (target variable to predict)                    |

# To prepare this data, the data was cleaned, and the following processes were performed:
# Exploratory Data Analysis
- During the exploratory data analysis, a boxplot and histogram was visualized for each numeric datatype column. 
- Also, a barplot was visualized for each categorical column. 
- This gave a good baseline for all of the numeric and categorical columns for univariate EDA.
![image](https://github.com/user-attachments/assets/af5eca2b-be4f-4213-9545-28671b1628b6)

Less price more Item sales

# Expanatory Data Analysis
- For visualizing the data, we selected two bar graphs, four line graphs, two box plots,one histoplot and one scatter plot.
- The bar graphs were used to compare the different categories.
- The line graphs were chosen to illustrate trends and draw conclusions.
- The box plots helped explore the distribution within each category and facilitate comparisons.
- Lastly, the scatter plot was selected to demonstrate the relationship between sales and outlet type overall.
## These visualizations collectively helped us understand the underlying trends, relationships, and distributions within the dataset.
![image](https://github.com/user-attachments/assets/0aba73d0-6feb-494b-80d5-d7beeccd7f1a)
 - The high quantity of sales of Fruits & vegetables, household, Snack foods resulted in high Item OUtlet Sales.
 - For the rest of Item Types, explore the item MRP.To explor  

![image](https://github.com/user-attachments/assets/e7a8a6b7-90de-4984-9d91-a9192fc4c811)
 - Through exploring the median values for Item MRP for each item type, we notice that Item MRP for Seafood and starchy foods have highest median (Prices) which explains the high OUtlet Item Sales.
 - Dairy with the highest range and equale distrbution
 - Seafood , Hard drinks and Household are with in the highest min Item_MPR(Price) range
![image](https://github.com/user-attachments/assets/642abdda-ac85-4e96-b410-59a05c613bf8)
 - For starchy foods, breakfast and snacks, the low fat items raised the Item MRP which led to a rise in Item Outlet Sales
 - Explor "Outlet_Identifier" to fined stores with the highest Outlet_Sales
![image](https://github.com/user-attachments/assets/89de8dc7-fa6f-4285-8875-e3bdfe4d7f5d)
 - Out027 (supermarket type 3) store achieved the highest Sales -Item_Outlet_Sales-Then:
 - Supermarket type 1|Supermarket type 2 |Grocery store
![image](https://github.com/user-attachments/assets/892db737-6f34-4275-9480-1f0d11d8a68f)
50% of the products in Supermarket type 3 achieved the highest Itemm Outlet Sales than the rest of the Outlet types. 
![image](https://github.com/user-attachments/assets/4f4a63d1-db81-411b-a343-2c7d834c6c0f)
 - The pattern of Item Outlet Sales in supermarket type 3 is higher in breakfast and fruits and vegetables compared to the rest of the supermarket patterns.
 - Supermarket type 2 has a higher pattern for seafood and hard drinks.
This resutled in a different pattern of Item Outlet Sales for these two supermarkets.
 - explor m Outlet Sales in supermarket type 3 is higher in breakfast and fruits and vegetables
![image](https://github.com/user-attachments/assets/953496e0-2c4d-429f-b4b9-5977eb05da7c)
 - The low fat breakfast type is the reason for scoring the highest Item_Outlet_Sales
 - Snack foods and Starchy Foods also scored higher Item_Outlet_Sales by the effect of low fat type
 ![image](https://github.com/user-attachments/assets/a7f05dc5-b048-4992-b40d-de092133d260)
 - There are four ranges for the Item_MRP distribution over Item out sales
 - The highest sales are at the two middle ranges of Item_MRP
![image](https://github.com/user-attachments/assets/6b92d3ff-115a-487d-902b-fcd2602e5974)
 - Dairy,Household and Starchy Foods score the hightest Item_MRP
 - Soft Drinks ,Baking Goods,Health & Hygiene ,and Ohters score the lowest Item_MRP
 - The rest of Outlet_Types are on the moderate range of Item_MRP
![image](https://github.com/user-attachments/assets/e247af4f-8833-4bb2-a05a-8417cc0cd63c)
 - Through exploring slopes, most Supermarket type 3's Item types are located in the 2nd and 3rd Item MRP ranges.
 - Distribution of Item types around the Supermarket type1 trend line seems like the average of the all the item outlet sales.
# Maching Learning Using the Following Models:
- Linear Regression Model
- Random Forest Regressor Model
- Tuned Random Forest Regressor Model
# Models Evaluated & Results
##Linear Regression Model 
- Regression Metrics: Test Data
 - MAE = 804.089
 - MSE = 1,194,326.602
 - RMSE = 1,092.853
 - R^2 = 0.567
## Default Random Forest Model
- Regression Metrics: Test Data
 - MAE = 765.671
 - MSE = 1,213,934.180
 - RMSE = 1,101.787
 - R^2 = 0.560
## Tuned Random Forest Model
- Regression Metrics: Test Data
 - MAE = 738.982
 - MSE = 1,130,203.386
 - RMSE = 1,063.110
 - R^2 = 0.590
# Item Outlet Sales Describe(target describe)
- count= 8523.00
- mean = 2181.29
- std = 1706.50
- min = 33.29
- 25% = 834.25
- 50% = 1794.33
- 75% = 3101.30
- max = 13086.96
For the testing set on the model, 59% of the variance in y was explained by x.
The Mean Absolute Error was off by about 739 items.
The Mean Squared Error was 1,130,203.
The Root Mean Squared Error had a calculation of 1,063 items.  
- Tuned Random Forest Model Observations is better than Random Forest and Linear Regression Model for test data.
- Item outlet sales Error of MAE=739 is still almost near to the 25% of the item outlet sales count which is a high score especially that min item score 33 items only.
# Using This Model to make predictions for item outlet sales which item outlets to choose to earn the highest outlet sales would not be a very reliable. Considering the previous regression metrics from how the model performed, there is a disparity in one of the model while out of performance for others. Considering the previous regression metrics from how the model performed.
 
