# 📊 Predicting Apartment Prices in Mexico City

## 🏙️ Project Overview
This project predicts the prices of apartments in Mexico City (Distrito Federal) using multiple datasets. The data undergoes extensive cleaning, preparation, and modeling to build a regression model that forecasts apartment prices based on size and location.

## 📂 Data
- Five CSV files containing real estate listings.
- Data includes apartment size, price, location (borough), and more.

## 🛠️ Tools & Libraries
- Python
- Libraries: -Pandas, NumPy, Seaborn, Matplotlib, Scikit-Learn, Category Encoders

## 📋 Data Processing Workflow
1. Import & Inspection
   - Read CSV files and inspect structure.
   - Identify columns with missing values and drop those with ≥ 50% null values.
2. Filtering
   - Focus on apartments (property_type).
   - Filter properties located in Mexico City (Distrito Federal).
3. Feature Engineering
   - Extract latitude (lat) and longitude (lon) from lat-lon column.
   - Create a new borough column from location hierarchy.
4. Handling Outliers
   - Apartments priced > $150k are excluded.
   - Filter apartments within the 10th-90th percentile for area (sq meters).
5. Categorical Columns
   - Drop low/high cardinality columns (operation, currency, etc.).
6. Target Leakage
   - Remove columns like price, price_aprox_local_currency, and price_per_m2 to avoid data leakage.
7. Final Dataset
   - Concatenate cleaned data from all CSV files.

## 📊 Exploratory Data Analysis
- Histograms visualize price distribution (right-skewed).
- Scatter plots show price vs. apartment area.

## 📈 Model Building
- Baseline Model: Predicts the average apartment price for all observations.
- Pipeline: Combines imputation, encoding, and regression.
- Linear Regression used as the primary model.

## 🚀 Results
- The model’s performance is evaluated using Mean Absolute Error (MAE).
- Results indicate the model can effectively estimate prices for affordable apartments in Mexico City.
