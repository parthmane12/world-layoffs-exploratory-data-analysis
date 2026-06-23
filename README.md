# World Layoffs Data Cleaning & Exploratory Data Analysis (SQL)

## Project Overview

This project analyzes global layoff trends using SQL by first performing comprehensive data cleaning and then conducting exploratory data analysis (EDA) on a dataset containing workforce reduction records from companies worldwide between 2020 and 2023.

The project demonstrates an end-to-end data analytics workflow, beginning with raw data preparation and progressing to business-focused insights through SQL queries, aggregations, window functions, and trend analysis.

---

# Objectives

The main objectives of this project were:

* Clean and prepare raw layoff data for analysis.
* Remove duplicate and inconsistent records.
* Standardize data formats and values.
* Handle missing and null values.
* Analyze layoff trends across companies, industries, countries, and time periods.
* Generate meaningful business insights from the cleaned dataset.

---

# Dataset Information

The dataset contains information about layoffs from companies around the world, including:

* Company Name
* Location
* Industry
* Total Employees Laid Off
* Percentage Laid Off
* Date
* Funding Stage
* Country
* Funds Raised (Millions)

Time Period Covered:

* March 2020 – March 2023

---

# Data Cleaning Process

Before performing exploratory analysis, extensive data cleaning was carried out to improve data quality and ensure reliable results.

## 1. Removing Duplicate Records

* Created staging tables to preserve the original dataset.
* Identified duplicate records using the `ROW_NUMBER()` window function.
* Removed duplicate rows while retaining unique records.

## 2. Standardizing Data

### Company Names

* Removed leading and trailing spaces using `TRIM()`.

### Industry Names

* Standardized industry categories.
* Consolidated variations of Crypto-related industries into a single value (`Crypto`).

### Country Names

* Removed unnecessary punctuation.
* Standardized country values for consistency.

### Date Formatting

* Converted date values from text format to SQL DATE format using `STR_TO_DATE()`.
* Changed the column datatype from TEXT to DATE.

## 3. Handling Missing Values

### Industry Values

* Replaced blank industry fields with NULL values.
* Populated missing industries using existing records from the same company.

### Incomplete Records

* Identified records where both:

  * Total Laid Off
  * Percentage Laid Off

  were missing.

* Removed records that could not contribute meaningful analytical value.

## 4. Removing Unnecessary Columns

* Dropped the helper column (`row_num`) used during duplicate detection.

---

# Exploratory Data Analysis

The cleaned dataset was analyzed to answer several business questions:

## Company Analysis

* Which companies laid off the most employees?
* Which companies experienced complete workforce reductions?
* What are the top-ranked companies by layoffs?

## Industry Analysis

* Which industries were most affected?
* How are layoffs distributed across sectors?

## Country Analysis

* Which countries experienced the highest layoffs?
* How does layoff activity vary geographically?

## Time-Series Analysis

* Monthly layoff trends.
* Yearly layoff trends.
* Peak layoff periods.

## Funding & Stage Analysis

* Relationship between funding raised and layoffs.
* Layoff patterns across company stages.

---

# SQL Concepts Used

* Data Cleaning Techniques
* CTEs (Common Table Expressions)
* Window Functions
* ROW_NUMBER()
* Aggregate Functions
* GROUP BY
* ORDER BY
* Date Functions
* Joins
* Ranking Analysis
* Data Standardization

---

# Key Insights

* The technology sector experienced some of the largest workforce reductions during the period analyzed.
* The United States recorded the highest number of layoffs among all countries.
* Several companies laid off their entire workforce, highlighting startup vulnerability during economic downturns.
* Layoffs increased significantly during periods of market correction and economic uncertainty.
* High funding levels did not necessarily protect companies from workforce reductions.
* Workforce reductions were concentrated in specific months, indicating broader market-wide trends.

---

# Tools Used

* MySQL
* SQL
* Window Functions
* Common Table Expressions (CTEs)

---

# Project Workflow

Raw Dataset
→ Data Cleaning
→ Data Standardization
→ Missing Value Treatment
→ Duplicate Removal
→ Exploratory Data Analysis
→ Business Insights

---

# Conclusion

This project demonstrates a complete SQL analytics workflow, starting with raw data cleaning and ending with business insight generation. Through data standardization, duplicate removal, null-value handling, and exploratory analysis, the project provides a clear picture of global layoff trends and showcases practical SQL skills used in real-world data analytics projects.
