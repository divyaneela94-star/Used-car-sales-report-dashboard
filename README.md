# 🚗 Used Car Sales Report — Power BI Dashboard

# 📘 Project Overview
This project analyzes used car sales data to identify and improve pricing strategies, sales performance, and market transparency in the pre-owned vehicle industry. The goal is to explore how various factors — such as make, model, year, mileage, and region — influence vehicle value and sales volume, ultimately helping dealerships optimize pricing and inventory decisions.

# 📊 Problem Statement
The analysis focuses on:
Evaluating factors affecting used car prices and sales.
Identifying regional performance trends and market transparency gaps.
Providing data-driven insights to improve sales strategy and vehicle pricing models.

# 🗂️ Data Sources
1.Primary Dataset: Kaggle – Used Car Sales Dataset  

2.GitHub Reference Dataset: divyaneela94-star/Used-car-sales-report-dashboard

# 🔍 Dataset Description
Each vehicle record includes:
Identification: Year, Make, Model
Specifications: Body Type (SUV, Sedan, etc.), Transmission (Automatic/Manual), Fuel Type (Petrol, Diesel, Electric)
Sales Data: Selling Price, Original Market Value, Mileage, City, State, Sales Source, and Number of Owners
The dataset provides the foundation for building an interactive Power BI dashboard that visualizes sales, pricing trends, and market dynamics.

# 🧹 Data Transformation & Cleaning
# 1.Key Insights from Raw Data
Pricing trends and depreciation patterns
Sales performance by make, model, and region
Value differences between original price and final selling price

# 2.🧰 Data Cleaning Steps (Performed in Excel & Power Query)
Text Standardization: Converted all text fields to Title Case (first letter capitalized).
Find & Replace: Fixed typos and inconsistencies in transmission, registration city, and state.

# Examples:
Manual → 0, Automatic → 1
Trichirappalli → Trichy, New Delhi → Delhi

IF(ISBLANK): Filled missing values for transmission, availability, price, and source columns.
IF Function: Replaced 0 values in Broker Quoter with “₹ 2,500”.
Date Conversion: Transformed AD_ON column to Short Date format.
Validation: Checked for duplicates, missing values, and formatting errors.
Power Query: Applied transformations for type consistency and derived metrics (Age, Price per KM).

# ⚙️ Tools & Technologies
Excel: Data cleaning, formulas, and initial validation.
Power Query: Advanced transformations and data modeling.
Power BI: Interactive dashboards and analytics.
GitHub: Version control and documentation.

# 📈 Power BI Dashboard Modules

# 1. Overall Sales Report
Total Units Sold, Revenue, Average Price
Sales trends by make, model, and fuel type

# 2. Regional Sales Report
City/State-based analysis with map visuals
Top-performing cities and regional demand hotspots

# 3. Sales Matrix
Pivot-style breakdown of sales by model, region, and transmission

# 4. KPI Section
Key performance metrics:
Total Revenue
Sales Volume
Average Selling Price
Depreciation Rate
Year-over-Year Growth

# 5. Dashboard Summary
Interactive Power BI visuals
Drill-throughs for make/model performance
Filters by region, year, and transmission type

# 📊 Key Measures (DAX Formulas)
1.Total Sales (Units) = COUNTROWS('Sales')
2.Total Revenue = SUM('Sales'[SellingPrice])
3.Average Price = DIVIDE([Total Revenue], [Total Sales (Units)], 0)
4.Depreciation Amount = SUMX('Sales', 'Sales'[OriginalPrice] - 'Sales'[SellingPrice])
5.Depreciation % = DIVIDE([Depreciation Amount], SUM('Sales'[OriginalPrice]), 0)
6.YoY Revenue = VAR Prev = CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Date'[Date]))
7.RETURN DIVIDE([Total Revenue] - Prev, Prev, BLANK())

# ✅ Validation & Quality Checks
Removed duplicates and invalid entries.
Checked for null values in key columns (Selling Price, Year, Mileage).
Ensured consistent city and state naming conventions.
Confirmed correct data types for numeric and date columns.

# 📅 Future Enhancements
Integration with real-time data via API.
Predictive modeling for price forecasting.
Enhanced visuals for sales funnel and inventory turnover.
Power BI web embedding for dashboard sharing.

# 🧠 Key Insights
Depreciation varies significantly by make, fuel type, and mileage.
SUVs and diesel vehicles maintain higher resale values.
Metro regions like Delhi and Mumbai have higher price variance.
Automatics show faster depreciation than manuals over time.

# ⭐ Acknowledgements

# 1.Kaggle 
for dataset sources.
# 2.Power BI Community
 for dashboard inspiration.
# 3.GitHub Repository Reference
 for baseline structure.

