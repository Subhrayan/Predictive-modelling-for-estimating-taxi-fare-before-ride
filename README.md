# Predictive modelling for estimating taxi fare before ride

## Purpose
To develop a predictive model that accurately estimates New York City taxi fares before rides using relevant data variables, enabling optimal pricing, enhancing customer satisfaction through transparent fares, and improving operational efficiency for the Taxi and Limousine Commission.


## 🔗 Links

### Dashboard Link : [Taxi Trip Analysis ](https://app.powerbi.com/view?r=eyJrIjoiZjgzODZmYTctZTMyZC00NTViLWEwNjgtYWRmNDE5MTQxYmFkIiwidCI6IjYwODIzNDA4LTBlYjktNGE0Zi04ZTcxLTY2MzcwYThmNjU4NSJ9&pageName=46bea8c8461a846987a8)

### Kaggle Notebook For more details: [Click Here To Visit Kaggle Notebbok](https://www.kaggle.com/code/subhrayansamajdar/predictive-model-for-taxi-fare/notebook)

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subhrayan-samajdar-78b17b132?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BKT08BcH3SnWhaOJFAjaQ1w%3D%3D)


[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://katherineoelsner.com/)





## PROJECT OVERVIEW

This project focuses on developing a predictive model to determine the fare amount for taxi cab rides in New York City area to ensure best customer experience based on data collected by The New York City Taxi and Limousine Commission.

### Problem
Estimating optimal taxi fares before the ride to promote customer-friendly practices.\ Question to be answered: What's the best the estimation of taxi fares based on relevant variables?

### Response
Since the variable to be predicted is continuous, a linear regression or tree-based machine learning model will be used.

### Impact
TLC can improve their operations based on the insights and also fair pricing will improve customer satisfaction.

### Data source
- The taxi Trip Data is stored in single csv file, can be accessed through - https://data.cityofnewyork.us/Transportation/2017-Yellow-Taxi-Trip-Data/biws-g3hs/about_data

- The dataset possesses the qualities of 'ROCCC'.

### Steps followed 

- step 1 : Data cleaning
- Step 2 : Exploration and descriptive analysis through EDA
- Step 3 : A/B test to analyze whether there is a relationship between payment type and fare amount.
- Step 4 : Building a multiple linear regression model
- Step 5 : Feature engineering for multiple linear regression model
- Step 6 : Building a machine learning models (Random Forest and XGBoost) 
- Step 7 : Feature engineering for Random Forest and XGBoost
- Step 8 : Modeling Random Forest
- Step 9 : Modeling XGBoost
- Step 10 : Loading data to Power Bi
- Step 11 : Building Dashboard

## Key Insights 
 1.
 ![newplot](https://github.com/Subhrayan/Bike-Share-analysis-SQL-and-Interactive-Power-BI-Dashboard/assets/154826702/f4752e20-01ab-40e4-8685-a1b63917bc4b)

The majority of trips were journeys of less than two miles. The number of trips falls away steeply as the distance traveled increases beyond two miles

2. 
![Screenshot 2024-06-12 212234](https://github.com/Subhrayan/Bike-Share-analysis-SQL-and-Interactive-Power-BI-Dashboard/assets/154826702/c51ab6cb-f437-4f41-ac67-97d260c7280a)

The total cost of each trip also has a distribution that skews right, with most costs falling in the $5-15 range.

3. 
![Screenshot 2024-06-12 212432](https://github.com/Subhrayan/Bike-Share-analysis-SQL-and-Interactive-Power-BI-Dashboard/assets/154826702/9777f23e-9e1a-4cf3-9d81-de1ffc636787)

The distribution for tip amount is right-skewed, with nearly all the tips in the $0-3 range.

4. 
![newplot (1)](https://github.com/Subhrayan/Bike-Share-analysis-SQL-and-Interactive-Power-BI-Dashboard/assets/154826702/15aea15e-9870-4a5a-ab29-f4cb288863e6)

Nearly two thirds of the rides were single occupancy, though there were still nearly 700 rides with as many as six passengers. Also, there are 33 rides with an occupancy count of zero, which doesn't make sense.

5. 
![Screenshot 2024-06-12 212824](https://github.com/Subhrayan/Bike-Share-analysis-SQL-and-Interactive-Power-BI-Dashboard/assets/154826702/d14d432a-03bc-433d-94d6-70e470b043f0)

Suprisingly, Wednesday through Saturday had the highest number of daily rides, while Sunday and Monday had the least.

6. 
![Screenshot 2024-06-12 212954](https://github.com/Subhrayan/Bike-Share-analysis-SQL-and-Interactive-Power-BI-Dashboard/assets/154826702/7981c215-e08f-429c-8d22-b3250f92c2b3)

Total revenue by day follows nearly similar trend as Ride count as day. Thursday had the highest gross revenue of all days, and Sunday and Monday had the least. Interestingly, although Saturday had only 35 fewer rides than Thursday, its gross revenue was ~$6,000 less than Thursday's—more than a 10% drop.

7. 
![Screenshot 2024-06-12 213705](https://github.com/Subhrayan/Predictive-modelling-for-estimating-taxi-fare-before-ride/assets/154826702/a9e62992-dfda-4a3d-8d78-a83125f927fb)

Monthly revenue generally follows the pattern of monthly rides, with noticeable dips in the summer months of July, August, and September, and also one in February.

8. There is a statistically significant difference in the average fare amount between customers who use credit cards and customers who use cash.

9. The multiple linear regression model performance is high on both training(0.84)  and test(0.83) sets, suggesting that there is little bias in the model and that the model is not overfit.

For the test data, an R2 of 0.83 means that 83% of the variance in the fare_amount variable is described by the model.
![Screenshot 2024-06-12 214539](https://github.com/Subhrayan/Predictive-modelling-for-estimating-taxi-fare-before-ride/assets/154826702/deff1ed2-a6c9-4213-92cc-53567d46d618)

![Screenshot 2024-06-12 214720](https://github.com/Subhrayan/Predictive-modelling-for-estimating-taxi-fare-before-ride/assets/154826702/c983fbe1-255f-42f6-b516-3c88cfaba47b)

The distribution of the residuals is approximately normal and has a mean of 0.052. The residuals represent the variance in the outcome variable that is not explained by the model. A normal distribution around zero is good, as it demonstrates that the model's errors are evenly distributed and unbiased.

10. From the coefficients of variables, it can be concluded that for every 3.60 miles traveled, the fare increased by a mean of $7.21. Or, reduced: for every 1 mile traveled, the fare increased by a mean of $1.98. 

11. Building random forest and xgboost models to predict whether or not a customer is a generous tipper.
![Screenshot 2024-06-12 215748](https://github.com/Subhrayan/Predictive-modelling-for-estimating-taxi-fare-before-ride/assets/154826702/f5f3cf80-95fa-47c0-995d-a72875944660)

12. Confusion matrix from XGBoost
![Screenshot 2024-06-12 215919](https://github.com/Subhrayan/Predictive-modelling-for-estimating-taxi-fare-before-ride/assets/154826702/d20aa103-217f-4359-b2af-d8261568c9ad)

13. Feature importance 
![Screenshot 2024-06-12 220013](https://github.com/Subhrayan/Predictive-modelling-for-estimating-taxi-fare-before-ride/assets/154826702/3510632c-d406-4a88-b394-bdfde53773a4)

14. Power Bi Dashboard 

![Screenshot 2024-06-12 220450](https://github.com/Subhrayan/Predictive-modelling-for-estimating-taxi-fare-before-ride/assets/154826702/04b3909b-28a2-4c94-9efa-e3c284a0ec63)
