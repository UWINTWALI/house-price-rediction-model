# House Sales Price Prediction

A machine learning project to predict house sale prices using property characteristics and historical sales data.

## Project Overview

RealAgents, a real estate company, needs to optimize listing prices for houses they're trying to sell. By predicting sale prices in advance based on house characteristics, they can decrease time-to-sale and stay competitive in the market.

This project analyzes historical housing data, cleans and preprocesses it, and builds predictive models to estimate sale prices.

## Dataset

The dataset contains records of previous house sales in a metropolitan area, including:

- **house_id**: Unique identifier for each house
- **city**: Location (Silvertown, Riverford, Teasdale, Poppleton)
- **sale_price**: Target variable - sale price in whole dollars
- **sale_date**: Date of the last sale
- **months_listed**: Time on market before sale
- **bedrooms**: Number of bedrooms
- **house_type**: Type of house (Terraced, Semi-detached, Detached)
- **area**: House area in square meters

## Tasks Completed

### 1. **Data Exploration & Missing Value Analysis**
- Identified missing values in the dataset
- Counted missing city entries (including '--' placeholders)

### 2. **Data Cleaning & Preprocessing**
- Standardized missing value handling across all columns
- Cleaned categorical data and text strings
- Converted data types appropriately
- Handled date formatting and numeric conversions

### 3. **Exploratory Data Analysis**
- Analyzed price distribution by number of bedrooms
- Calculated average prices and variance by property features
- Generated insights for the business team

### 4. **Predictive Modeling**
Built two different models to predict house sale prices:

#### **Model 1: Baseline Model**
- Simple linear regression using only bedrooms as predictor
- Establishes a performance benchmark
- Purpose: Quick, interpretable predictions

#### **Model 2: Comparison Model**
- Random Forest Regressor with tuned hyperparameters
- Uses all available features: bedrooms, area, months_listed, city, house_type
- Includes proper preprocessing (OneHotEncoding for categorical variables)
- More sophisticated approach for improved accuracy

## Model Performance

The models' performance is evaluated using Root Mean Squared Error (RMSE). At least one model must achieve RMSE below $30,000 to meet the business requirement.

### Modeling Approach:
1. **Feature Selection**: Identified key predictors of house prices
2. **Preprocessing Pipeline**: Built reusable data transformation pipelines
3. **Model Training**: Trained models on historical data
4. **Prediction**: Generated price estimates for new properties


## Key Insights

1. **City matters**: Location significantly impacts house prices
2. **House type hierarchy**: Detached > Semi-detached > Terraced (price-wise)
3. **Bedrooms aren't everything**: While important, other features like area and location play crucial roles
4. **Market timing**: Months listed affects sale price, suggesting pricing strategy importance

## Business Impact

By accurately predicting house prices, RealAgents can:
- Set optimal listing prices from the start
- Reduce time properties spend on the market
- Make data-driven pricing decisions
- Improve client satisfaction with faster sales