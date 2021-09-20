# Supplement-Sales-Prediction
Your Client WOMart is a leading nutrition and supplement retail chain that offers a comprehensive range of products for all your wellness and fitness needs. 

WOMart follows a multi-channel distribution strategy with 350+ retail stores spread across 100+ cities. 

Effective forecasting for store sales gives essential insight into upcoming cash flow, meaning WOMart can more accurately plan the cashflow at the store level.

Sales data for 18 months from 365 stores of WOMart is available along with information on Store Type, Location Type for each store, Region Code for every store, Discount provided by the store on every day, Number of Orders everyday etc.

Your task is to predict the store sales for each store in the test set for the next two months.

Train Data	
ID - Unique Identifier for a row
Store_id - Unique id for each Store
Store_Type - Type of the Store
Location_Type - Type of the location where Store is located
Region_Code - Code of the Region where Store is located
Date - Information about the Date
Holiday	- If there is holiday on the given Date, 1 : Yes, 0 : No
Discount	- If discount is offered by store on the given Date, Yes/ No
#Orders - 	Number of Orders received by the Store on the given Day
Sales	- Total Sale for the Store on the given Day
	
Test Data	
Variable - Definition
ID - Unique Identifier for a row
Store_id - Unique id for each Store
Store_Type - Type of the Store
Location_Type -	Type of the location where Store is located
Region_Code - 	Code of the Region where Store is located
Date - Information about the Date
Holiday - If there is holiday on the given Date, 1 : Yes, 0 : No
Discount - If discount is offered by store on the given Date, Yes/ No

Approach

1. There are no null values and duplicate values in dataset
2. Have split date column in 3 feature - month,date and year
3. Used label encoding on column store Type, Location_Type ,Location_Type,Region_Code and Region_Code
4. Split the data, used 80% of data training and 20 for testing
5. Created 3 model  - Linear Regression ,  RandomForestRegressor  and XGBoost Regressor
6. XGBoost Regressor was selected with following paramater
n_estimators=700, max_depth=16,learning_rate =0.01,min_child_weight=0.5,  colsample_bytree=0.8,subsample=0.8,gamma=0.01

