
## PHASE 5 CAPSTONE PROJECT PROPOSAL
    GROUP 9
## MEMBERS:
    1. ANGELA MWANZIA
    2. REAGAN ADAJO
    3. DANIEL MUIGAI
    4. SAMUEL KAMAU
    5. RONALD OGWANG
    6. FILDA KIARIE

## TOPIC: Retail Demand Forecast

### Project Overview
We propose to develop a machine learning solution to accurately forecast customer demand across multiple retail locations, optimizing inventory management and reducing operational inefficiencies. Using 25 months of historical sales data from four stores, we'll create predictive models that capture complex patterns in customer purchasing behavior, price sensitivity, and promotional impacts.
### Objectives
1. Develop a machine learning model that accurately predicts product demand across multiple store locations.

2. Identify Key Factors influencing customer purchasing patterns

3. Understand the impact of pricing strategies, promotions and markdowns on sales volumes
### Data Sources
The project integrates diverse data sources, including in-store and online sales, price changes, markdowns, promotional history, product catalog information, and store-specific details. Our analysis will leverage datasets spanning 25 months of historical sales data from four retail stores:

1. In-store Sales Data (sales.csv): Daily sales records including quantity sold, pricing, and revenue metrics
2. Online Sales Data (online.csv): Store-specific e-commerce transaction data
3. Pricing Information: 
o	price_history.csv: Historical price changes by product and store
o	markdowns.csv: Records of discounted product sales
o	discounts_history.csv: Detailed promotional pricing history
4. Product Information: 
o	catalog.csv: Product details including department, class, and specifications
o	actual_matrix.csv: Store-specific product availability data
•	Store Information (stores.csv): Comprehensive store details including format, location, and size
### Technical Approach
1.	Data Preparation 
o	Clean and integrate multiple data sources
o	Handle missing values and outliers
o	Create unified dataset for analysis
2.	Feature Engineering 
o	EDA & visualization
o	Develop temporal features (trends, seasonality)
o	Create price sensitivity metrics
o	Incorporate product and store characteristics
o	Generate lag and rolling window features
3.	Model Development 
o	Implement a machine learning model
o	Apply time series forecasting techniques
o	Evaluate model performance
o	Identify key demand drivers
### Evaluation Metric
•	Model performance will be evaluated using Root Mean Squared Error (RMSE). Lower RMSE values indicate more accurate prediction model.


   






