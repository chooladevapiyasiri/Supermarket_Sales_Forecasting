
## Executive Summary

This project develops a robust machine learning pipeline to predict next-week sales for the top 5 fast-moving categories across selected supermarket departments and stores.

**Target departments include:**

- Grocery
- Beverages
- Chilled

**Target outlets:**

- Store A
- Store B
- Store C
- Store D
- Store E

The objective is to improve inventory optimization, replenishment planning, and supply chain efficiency by leveraging historical transactional data and structured forecasting techniques.

## Business Problem

Retail environments require accurate short-term forecasts to:

- Prevent stockouts
- Reduce overstocking
- Optimize working capital
- Improve customer satisfaction
- Traditional rule-based replenishment methods fail to capture:
- Weekly seasonality
- Store-level variations
- Category-level demand fluctuations
- Promotion-driven demand shifts

This project addresses these limitations through a data-driven forecasting framework.

## Exploratory Descriptive Analysis (EDA):
   - Explored historical sales data to identify trends, patterns, and correlations.  
   - Validated assumptions and ensured data quality using descriptive statistics, visualizations, and hypothesis testing.  
   - Determined key drivers affecting sales across departments and stores.

EDA ensured that modelling assumptions were grounded in data behavior rather than guesswork.

## Pipeline Design

The entire workflow is modularized inside the src/ directory.

- **Data Processing:** Clean and preprocess raw data to generate model-ready inputs.
- **Primary Keys:** Identify unique identifiers such as outlet, item category, and week.
- **Target Variable:** Define sales for the next week as the prediction target.
- **Feature Engineering:** Create features based on sales history, item characteristics, time, and outlet information.
- **Pipeline Creation (src/ folder):** Modular pipeline for preprocessing, feature engineering, and model training.
- **Model Training & Evaluation:** Train predictive models and evaluate performance using **Mean Absolute Percentage Error (MAPE)** at the granularity of **Outlet | Item Category | Week**.

## Key Outcomes

- Provides **accurate sales forecasts** for top-selling categories.  
- Enables better **inventory planning and stock optimization**.  
- Supports **supply chain management** by predicting customer demand effectively.  
- Modular pipeline allows easy **scalability and adaptation** for additional stores or categories.

## Tech Stack

- **Programming:** Python  
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn  
- **Architecture:** Modular ML pipeline (src/ structure) 
- **Evaluation Metrics:** Mean Absolute Percentage Error (MAPE)  

## Scalability & Future Improvements

Potential extensions:

- Add promotion and pricing data
- Integrate weather effects
- Use advanced models (XGBoost, LightGBM)
- Implement hierarchical forecasting
- Deploy via API for real-time inference
- Add automated retraining workflow
