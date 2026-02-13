# Project Title: Blinkit Sales Analysis & Prediction (Python)
### Overview
This project analyzes Blinkit retail data (8,523 rows × 12 columns) to identify key drivers of sales and build a machine learning model to predict item sales. The workflow includes data cleaning, exploratory data analysis, statistical testing (ANOVA + Tukey HSD), feature engineering, and model building.
### Dataset Columns
- Item Fat Content, Item Identifier, Item Type
- Outlet Establishment Year, Outlet Identifier, Outlet Location Type, Outlet Size, Outlet Type
- Item Visibility, Item Weight, Sales, Rating
### Objectives
- Understand what factors drive sales across products and outlets
- Validate category-level sales differences using statistical tests
- Engineer meaningful features (Outlet Age, Visibility Ratio, etc.)
- Build and evaluate regression models to predict Sales
### Key Steps
### 1. Data Cleaning
   - Standardized inconsistent labels (e.g., fat content)
   - Imputed missing values (median for skewed weight)
   - Treated Item Visibility = 0 as missing and imputed by Item Type mean
### 2. EDA
   - Total Sales by Fat Content
   - Sales patterns across Item Type and Outlet Type
   - Total Sales across Outlet Establishment Years
   - Total Sales contribution across Outlet Location Type by Fat Content
   - Item Fat Content vs Item Type
   - Visualized the relationship between Rating and Item Visibility w.r.t Sales
### 3. Statistical Testing
   - One-way ANOVA for Item Type vs Sales
   - Tukey HSD to identify which categories differ significantly
   - One-way ANOVA for Outlet Type vs Sales
### 4. Feature Engineering
   - Outlet Age from establishment year (data-driven reference year)
   - Visibility Ratio (relative visibility within item type)
   - Item Identifier Type (FD/DR/NC → Food/Drinks/Non-Consumable)
### 5. Modeling & Evaluation
   - Linear Regression (baseline), Gradient Boosting, Random Forest
   - Best model: Random Forest (R² = 0.54, MAE = 31.31, RMSE = 42.57)
   - Feature importance highlights: Item Weight, Visibility Ratio, Item Visibility, Rating, Outlet Age
   - Retail sales forecasting is inherently noisy and many key drivers such as pricing, promotions, and seasonality are not present in the dataset. Therefore, achieving an R² of 0.54 indicates that the model captures meaningful sales patterns and represents strong performance for the available data.
### Results & Insights
- Total sales are highest for Supermarket Type1 outlets.
- Item categories significantly impact sales; top categories include Dairy, Fruits & Vegetables, Snack Foods, Household.
- Visibility-related features are among the strongest predictors of sales.
### Tech Stack
- Python: pandas, numpy, matplotlib, seaborn
- Stats: scipy, statsmodels
- ML: scikit-learn
### How to Run
#### 1. Clone the repo
#### 2. Install requirements
#### 3. Open the notebook and run cells top-to-bottom
