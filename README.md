# Pandas_Data_Processing-Python

This repository contains my homework submission for practicing **Pandas data processing, cleaning, and exploratory analysis** using a small census dataset. The assignment involved working with real-world quirks in the data such as missing values, duplicates, and messy column labels, while performing a range of analytical and transformation tasks.

---

### Business Problem

Accurate and clean data is essential for making sound business decisions. This project simulated real-world data preprocessing challenges, using **US Census population data** (2010–2019) for all 50 states, the District of Columbia, and Puerto Rico.
The tasks involved transforming raw census data into a clean, structured format ready for further analysis or machine learning, a common challenge for data scientists.

---

### Dataset Overview

The dataset, `census_statespop.csv`, included:

- **Region**: Census region of the state (Northeast, South, Midwest, West)
- **Population columns**: Yearly population from 2010 to 2019
- **Issues**:  
  - Missing values (e.g., for some territories like Puerto Rico)
  - Duplicate rows
  - Messy column names
  - Mixed data types (floats instead of integers)

---

### Project Objective

This assignment aimed to:

- Import, clean, and preprocess data using Pandas  
- Handle missing data and duplicates  
- Rename columns systematically  
- Perform Boolean and conditional indexing  
- Apply transformations like aggregation, sorting, and mathematical calculations  
- Create new computed columns (e.g., CAGR, coefficient of variation)  
- Export and re-import cleaned data
- Practice chaining, apply(), groupby(), and aggregation operations

---

### Solution Approach

**1. Data Import and Exploration:**
- Used `pd.read_csv()` to load and reformat column names dynamically
- Inspected data types, shapes, null values, and structure
- Displayed subsets of data with head(), tail(), and slicing

**2. Data Cleaning:**
- Identified and removed all-null rows and duplicate records
- Imputed missing values for regions where appropriate
- Made deep copies of cleaned DataFrames for safety

**3. Data Manipulation and Feature Engineering:**
- Renamed columns systematically (e.g., `y2010`, `y2011`, ...)
- Created new columns:
  - **RegionAll**: Filled missing region information
  - **CAGR**: Compound Annual Growth Rate between 2015 and 2019
  - **coeffofvar**: Coefficient of Variation across 2010–2019 population
  - **mean2019popbyReg**: Mean 2019 population grouped by region

**4. Data Analysis and Indexing:**
- Performed Boolean indexing and filtering based on various conditions
- Aggregated and grouped data using `.groupby()`, `.agg()`, and `.transform()`
- Applied complex functions row-wise using `apply()`

**5. File I/O Operations:**
- Saved cleaned DataFrames back to CSV
- Re-imported and corrected datatypes for integer columns

---

### Business Value

Data preprocessing is a critical phase in the machine learning pipeline.  
This project demonstrates the ability to:

- **Detect and fix real-world data issues** before analysis
- **Create engineered features** for improved predictive modeling
- **Improve data consistency** and **reduce bias** introduced by missing or duplicated records
- **Automate cleaning workflows** using Python and Pandas

---

### Challenges Encountered

- Handling missing values correctly across both rows and columns
- Keeping track of column renaming without manually typing every name
- Dealing with data type conversions when exporting/importing data
- Designing transformations to create accurate summary features

---
