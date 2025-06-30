# Indian Urban Census Analysis using SQL Server & Python

This project explores and analyses urban population growth in Indian cities between the 2001 and 2011 censuses, using data scraped from Wikipedia. It demonstrates end-to-end data handling — from extraction and cleaning to SQL-based analytics — to uncover key trends in city and state-wise urbanisation.

## 📌 Problem Statement
India's rapid urbanisation between 2001 and 2011 is not easily analyzable using raw data. This project solves that by transforming Wikipedia census tables into a structured format ready for SQL Server analysis.

## Dataset Description
Source: Wikipedia (List of cities by population)
Includes:
  - City name
  - State or Union Territory
  - Population (2001 & 2011)
  - Calculated growth rate
  - Tier classification (Above 1M, 100k–1M)

## 🛠️ Tools Used
- Python (Pandas, BeautifulSoup)
- SQL Server

## 🧹 Project Pipeline
- **Data Extraction**: Scraped population data using `pandas.read_html()` from Wikipedia
- **Cleaning**: Removed unwanted characters, converted populations to integers
- **Merging**: Combined Tier-1 and Tier-2 datasets
- **Transformation**: Calculated `growth_rate` column in %
- **Loaded to SQL Server**
- **Analysis**: 
  - Top 10 fastest-growing cities
  - State-wise total urban growth
  - Tier-based comparisons
  - Cities with negative or stagnant growth
- **Future Scope**:
  - Add 2021 census data
  - Power BI Dashboard
  - ML prediction on city population growth
  - Migration & literacy-based expansion

## Folder Structure

```bash
  data/
    └── indian_cities_cleaned.csv
  scripts/
    ├── web_scraping.ipynb
    └── data_cleaning_merge.py
  sql/
    ├── create_table.sql
    ├── insert_data.sql
    └── analysis_queries.sql

