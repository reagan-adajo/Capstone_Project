
## PHASE 5 CAPSTONE PROJECT


## TOPIC: Retail Demand Forecast

### Project Overview
We proposed to develop a machine learning solution to accurately forecast customer demand across multiple retail locations, optimizing inventory management and reducing operational inefficiencies. Using 25 months of historical sales data from four stores, we'll create predictive models that capture complex patterns in customer purchasing behavior, price sensitivity, and promotional impacts.
### Objectives
1. Develop a machine learning model that accurately predicts product demand across multiple store locations.

2. Identify Key Factors influencing customer purchasing patterns

3. Understand the impact of pricing strategies, promotions and markdowns on sales volumes
### Data Sources
The project integrates diverse data sources, including in-store and online sales, price changes, markdowns, promotional history, product catalog information, and store-specific details. Our analysis will leverage datasets spanning 25 months of historical sales data from four retail stores:

Source Link: https://www.kaggle.com/competitions/ml-zoomcamp-2024-competition/data


### Technical Approach
1.	Data Preparation 
    1.Negative values in the sales columns (quantity, priceBase, sum_total) Action: Drop rows
    2.Covert date column for all dataframes into date_time
    3.introduce a column called source in the sales data
    4.merge online_sales and offline_sales as they have the same column names

2.	Feature Engineering 
o	EDA & visualization

![Quantity Sold in Different Stores](image.png)
![Quantity Sold Over Time](image-1.png)

o	Develop temporal features (trends, seasonality)
We aggregated features at different levels (store, item, department, and class) to capture sales trends across multiple hierarchies. 
These aggregations help in understanding demand patterns at various granularities, improving forecast accuracy.

- Store-level: Captures overall store demand fluctuations.

- Item-level: Helps in identifying item-specific trends.

- Department/Class-level: Identifies category-wide trends to capture broader market shifts.

3.	Model Development 

We Trained and evaluated a LightGBM model for demand forecasting.


### Evaluation Metric
o	Model performance
Validation RMSE: 1.1625
Validation MAE: 0.2745

o	Identify key demand drivers
![Feature Importance](image-2.png)


## Deployment
