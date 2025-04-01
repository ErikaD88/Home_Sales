# Home Sales Analysis with SparkSQL

This project uses Apache Spark and SparkSQL to perform data analysis on a dataset of home sales. The analysis includes computing average home prices under different conditions, working with temporary tables, caching, and optimizing queries with partitioning and Parquet formats.

## Objective

The objective of this challenge is to use SparkSQL to determine key metrics from home sales data. You'll practice reading data from an AWS S3 source, creating temporary views, caching and uncaching tables, and performing performance comparisons.

## Dataset

- **Source:** Provided via AWS S3 bucket.
- **Format:** CSV, later saved in Parquet format.
- **File:** `home_sales_revised.csv`

## Instructions & Steps

1. **Setup and Initialization**
   - Clone this repository.
   - Open `Home_Sales.ipynb`.
   - Import necessary PySpark SQL functions.

2. **Data Loading**
   - Read `home_sales_revised.csv` into a PySpark DataFrame.
   - Create a temporary view called `home_sales`.

3. **SparkSQL Queries**
   - Calculate average price for four-bedroom homes sold per year.
   - Calculate average price for homes (3 bed / 3 bath) per year built.
   - Calculate average price for 3 bed / 3 bath / 2 floors / ≥2000 sqft homes per year built.
   - Calculate average price of home per view rating with an average price ≥ $350,000 and record query runtime.

4. **Caching & Performance**
   - Cache the `home_sales` temporary table.
   - Re-run the previous query using cached data and compare runtimes.
   - Partition the data by `date_built` and save as Parquet.
   - Create a temporary view from the Parquet data and re-run the query to compare runtimes again.
   - Uncache and verify uncaching of the `home_sales` temporary table.

## Deliverables

- Jupyter Notebook: `Home_Sales.ipynb`
- Analysis and results including runtime comparisons
- Repository with all necessary files pushed to GitHub

## Technologies Used

- Python
- PySpark
- SparkSQL
- Jupyter Notebook
- AWS S3
- Parquet Format
