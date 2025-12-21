# Prediction-of-Product-Sales
This project aims to predict the sales of food items in various stores
## Introduction
# Sales Predictions 2023 Analysis

This project analyzes the sales_predictions_2023.csv dataset to predict sales and find trends. It uses Python libraries such as pandas, numpy, matplotlib, and seaborn for data cleaning, exploration, and visualization.

## 1. Data Exploration

### Initial Data Inspection
This step is to gather first insight of the data (number of columns and the number of the rows) and what are the data types in the dataframe.
- **Rows**: 8523
- **Columns**: 12
- **Data Types**: Mixture of object (categorical), float, and integer.

#### first insight if that:
**Insight**: The dataset is a mix of numerical and categorical variables. Key outcome variable is Item_Outlet_Sales. Some columns like Item_Weight and Outlet_Size have missing values.

### Summary Statistics
- **Item_Outlet_Sales**: Ranging from 33.29 to 13086.96 with a mean of 2181.29.
- **Item_MRP**: Ranges from 31.29 to 266.89.

## 2. Data Cleaning

### Duplicates
- **Result**: No duplicates found.

### Missing Values
- **Identified**:
    - Item_Weight: 1463 missing values.
    - Outlet_Size: 2410 missing values.
- **Action**: Filled missing Outlet_Size (categorical) with 'MISSING'.
- **Action**: Filled the missing Item_Weight with mean of this Column.
**Insight**: Filling categorical missing values with a placeholder like 'MISSING' allows the data to be retained while acknowledging the absence of information.

### Inconsistencies
- **Identified**: Item_Fat_Content contained 'LF', 'low fat', 'Regular', 'reg', 'Low Fat'.
- **Action**: Standardized to 'Low Fat' and 'Regular'.

**Insight**: Uniform labels are crucial for accurate grouping and analysis.

## 3. Visualizations and Insights

### Correlation Heatmap

