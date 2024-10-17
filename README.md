# Real Estate Price Prediction and Analysis Project

## Overview

This project aims to support a real estate company expanding from California into the Slovakian market by integrating data from both regions, analyzing property trends, and building a predictive machine learning model to estimate property prices in Slovakia. The analysis and insights are presented through interactive Tableau dashboards to facilitate data-driven decision-making for company executives.

## Project Structure

1. **Data Integration**: Combined California and Slovakia datasets into a unified format.
   - California data includes broad socio-economic factors such as median income, population, and property prices.
   - Slovak dataset includes detailed property-specific information like type, number of rooms, price, and condition.

2. **Data Cleaning and Transformation**: Cleaned the data, handled missing values, and transformed the features to align both datasets for better comparability.
   - Created a new column, `MedInc`, to represent the median income in Slovakia using proxy information based on property prices and conditions.
   - Normalized property prices between California and Slovakia.

3. **Feature Engineering**:
   - Created new features, such as `AveBedrms` and `AveRooms`, to match the California dataset’s schema.
   - Combined datasets with columns like `MedInc`, `HouseAge`, `AveRooms`, `AveBedrms`, `AveOccup`, `Price`, and `Country`.

4. **Machine Learning Model**: Developed a model to predict property prices in new regions.
   - Models tried: **Linear Regression**, **Decision Tree Regressor**, and **Gradient Boosting Regressor**.
   - Best Model: **Gradient Boosting Regressor**, selected based on **MAE**, **RMSE**, and **R2** scores.
   - Conducted **Hyperparameter Tuning** using **GridSearchCV** to improve model performance.

5. **SQL Database Setup**:
   - Created an SQL database using **SQLAlchemy** to store the integrated dataset.
   - Designed a **normalized schema** with separate tables for `Property`, `Location`, `Price`, and `Feature` to minimize redundancy and optimize performance.
   - Verified table creation and structure with database visualization tools.

6. **Data Visualization Using Tableau**:
   - Created an **interactive Tableau dashboard** to visualize property trends and provide actionable insights.
   - Key Metrics Visualized:
     - **Property Price Distribution**: Comparison between California and Slovakian property prices.
     - **Property Features**: Breakdown of property types, sizes, and amenities.
     - **Geographical Trends**: Visualization of price differences across neighborhoods.
     - **Investment Opportunities**: Highlighted areas for profitable investments based on median income and pricing.

## Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/real-estate-price-prediction.git
   cd real-estate-

