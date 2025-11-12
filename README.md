# Used-car-sales-report-dashboar
In this Used car sales report my project in power bi, i have upload my project

# 📘 Project Overview
This project analyzes used car sales data to identify and improve pricing strategies, sales performance, and market transparency in the pre-owned vehicle industry. The goal is to explore how various factors — such as make, model, year, mileage, and region — influence vehicle value and sales volume, ultimately helping dealerships optimize pricing and inventory decisions.

# 📊 Problem Statement
The analysis focuses on:
Evaluating factors affecting used car prices and sales.
Identifying regional performance trends and market transparency gaps.
Providing data-driven insights to improve sales strategy and vehicle pricing models.

# 🗂️ Data Sources
Primary Dataset: Kaggle – Used Car Sales Dataset
GitHub Reference Dataset: divyaneela94-star/Used-car-sales-report-dashboard

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
