# US Home Prices Analysis

## Overview
This project analyzes the factors influencing home prices in the United States over the last 20 years. Using the S&P Case-Schiller Home Price Index as a proxy for home prices, the goal is to build a data science model to explain the relationship between key economic factors and home prices.

### Objective:
- Collect and clean publicly available data that influences home prices.
- Perform exploratory data analysis (EDA) to understand trends and relationships.
- Build a data science model that explains how these factors impacted home prices from 2000 to 2025.

## Data Sources
The data used in this project is sourced from publicly available databases. The primary dataset for home prices is the **S&P Case-Schiller Home Price Index** from the [Federal Reserve Economic Data (FRED)](https://fred.stlouisfed.org/series/CSUSHPISA).

Additional datasets related to economic factors are sourced from:
- US GDP Data
- Interest Rates from the Federal Reserve
- Unemployment Rate from US Bureau of Labor Statistics
- Inflation Rate from US Bureau of Labor Statistics
- Housing Inventory Data (e.g., US Census Bureau)

## Project Structure

```bash
your-project-folder/
│
├── .gitignore               # Ignored files and directories
├── LICENSE                  # Open source license (MIT)
├── README.md                # Project documentation
├── requirements.txt         # List of dependencies
│
├── data/
│   ├── raw/                 # Raw data fetched from APIs
│   └── processed/           # Cleaned data ready for analysis
│
├── notebooks/
│   ├── 01_data_collection.ipynb  # Fetch and save raw data
│   ├── 02_eda.ipynb            # Exploratory Data Analysis
│   ├── 03_modeling.ipynb       # Model development and evaluation
│
└── outputs/
    ├── charts/             # Visualizations
    └── final_report.md     # Summary of findings and insights

