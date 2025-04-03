
# Sales Demand Forecasting

This repository contains a Jupyter Notebook that demonstrates the process of building a demand forecasting model for a retail business. The model leverages historical sales data, engineered features, and the LightGBM algorithm to predict future item demand at the store level.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Dataset Description](#dataset-description)
- [Features Engineering](#features-engineering)
- [Modeling Approach](#modeling-approach)
- [Evaluation Metrics](#evaluation-metrics)
- [Results & Insights](#results--insights)
- [How to Run the Project](#how-to-run-the-project)
- [Conclusions & Recommendations](#conclusions--recommendations)
- [Future Work](#future-work)
- [Dependencies](#dependencies)
- [License](#license)

---

## Project Overview

The primary goal of this project is to develop an accurate and scalable sales demand forecasting model. By analyzing historical sales data and applying advanced feature engineering techniques, the model supports better inventory management, pricing strategies, and promotional planning for retailers.

---

## Objectives

- **Accurate Demand Prediction:** Build a model that forecasts future demand using historical sales data.
- **Inventory Optimization:** Provide insights to reduce stockouts and overstock situations.
- **Seasonality & Trend Analysis:** Incorporate time-based features (lags, moving averages, seasonal indices) to capture both short-term and long-term demand patterns.
- **Operational Efficiency:** Enable data-driven decision-making in store-level operations and supply chain management.

---

## Dataset Description

The dataset includes sales records from multiple stores over a period of 25 months. Key data fields include:
- **item_id:** Identifier for each product.
- **quantity:** Quantity sold.
- **store_id:** Identifier for each store.
- **date:** Date of the transaction.
- **store_quantity:** Store-level aggregated quantity.
- **item_quantity:** Item-level aggregated quantity.
- **Time-based features:** Day of week, weekend flag, month, quarter.
- **Lag features:** For 1, 7, 14, and 28 days.
- **Moving averages:** 7-day, 14-day, 28-day moving averages.
- **Seasonal indices:** Year-over-year (YoY) metrics and average quantities by day-of-week, month, and quarter.

---

## Features Engineering

Key features developed include:

- **Lag Features:** `quantity_lag_1`, `quantity_lag_7`, etc., to capture recent trends.
- **Moving Averages:** `quantity_ma_7d`, `quantity_ma_14d`, `quantity_ma_28d` to smooth out short-term fluctuations.
- **Seasonal Indicators:** `dow_avg_quantity`, `month_avg_quantity`, `quarter_avg_quantity`, `quantity_seasonal_idx` to capture recurring seasonal patterns.
- **Interaction Features:** (Optional) Interaction between lag values and seasonal indices to capture complex relationships.

These engineered features play a critical role in capturing both immediate and historical trends, which are essential for accurate forecasting.

---

## Modeling Approach

The forecasting model is built using LightGBM, a gradient boosting framework that handles large datasets efficiently. Key aspects include:

- **Parameter Tuning:** Optimization of hyperparameters (e.g., learning rate, num_leaves) to minimize forecasting error.
- **Validation Strategy:** Implementation of time series cross-validation to simulate real-world forecasting scenarios.
- **Handling Warnings:** Addressing parameter conflicts (e.g., feature_fraction and colsample_bytree) to ensure model integrity.

---

## Evaluation Metrics

The model's performance is evaluated using:

- **RMSE (Root Mean Squared Error):** Measures the average magnitude of error, penalizing larger deviations.
- **MAE (Mean Absolute Error):** Provides the average absolute difference between predictions and actual values.
  
Additional metrics such as MAPE and sMAPE can be incorporated for a relative evaluation, and R-squared helps assess the proportion of variance explained by the model.

---

## Results & Insights

- **Model Performance:**  
  - **Validation RMSE:** 0.7923  
  - **Validation MAE:** 0.5806  
  These metrics indicate that the model has good predictive accuracy relative to the scale of the data.
  
- **Feature Importance:**  
  Top features include `item_quantity`, `quantity_lag_1`, and `store_quantity`. This emphasizes that recent sales trends and seasonality strongly influence demand forecasts.

- **Business Impact:**  
  Enhanced forecasting can drive better inventory management, targeted promotional strategies, and overall operational efficiency.

---

## How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/sales-demand-forecasting.git
   cd sales-demand-forecasting
   ```
2. **Set Up the Environment:**
   - Create a virtual environment and install dependencies:
     ```bash
     python -m venv venv
     source venv/bin/activate  # On Windows use `venv\Scripts\activate`
     pip install -r requirements.txt
     ```
3. **Run the Notebook:**
   - Launch Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Open and run `Gold-edit.ipynb` to view the analysis and model training steps.
   
4. **Hyperparameter Tuning:**
   - Optional: Run the provided Optuna scripts to fine-tune model parameters.

---

## Conclusions & Recommendations

- **Conclusions:**  
  The developed model shows strong performance with low RMSE and MAE values. Feature importance analysis validates the significance of historical sales trends and seasonality. The approach scales well and can be integrated into operational systems for enhanced decision-making.

- **Recommendations:**  
  - **Model Deployment:** Integrate the forecasting model into real-time systems for inventory management and pricing strategy optimization.
  - **Data Expansion:** Incorporate additional external factors such as promotions, holidays, and weather data to further refine the forecasts.
  - **Continuous Improvement:** Regularly update and retrain the model using new data and explore ensemble methods for potential performance gains.
  - **Stakeholder Engagement:** Use model insights to drive targeted business strategies, ensuring all departments are aligned with data-driven practices.

---

## Future Work

- **Explore Hybrid Models:** Investigate combining tree-based methods with statistical approaches.
- **Advanced Feature Engineering:** Develop more sophisticated interaction features and consider deep learning approaches.
- **Real-Time Forecasting:** Set up pipelines for real-time data ingestion and forecasting.

---

## Dependencies

- Python 3.x
- [pandas](https://pandas.pydata.org/)
- [numpy](https://numpy.org/)
- [LightGBM](https://lightgbm.readthedocs.io/)
- [scikit-learn](https://scikit-learn.org/)
- [Optuna](https://optuna.org/)
- [Jupyter Notebook](https://jupyter.org/)

*For a complete list, see the `requirements.txt` file.*

---

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to reach out if you have any questions or need further assistance with the project. Happy forecasting!

---