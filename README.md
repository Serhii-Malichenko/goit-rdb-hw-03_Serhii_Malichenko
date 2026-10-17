# goit-rdb-hw-03_Serhii_Malichenko
# Seoul Bike Sharing Demand — Data Import and Analysis

## Project Overview

This project explores the **Seoul Bike Sharing Demand** dataset and demonstrates a complete data workflow, from obtaining source data to loading, cleaning, validating, and analysing it using Python and PostgreSQL.

The objective is to prepare a structured dataset suitable for further analysis and to investigate factors associated with bike rental demand.

## Dataset Information

- **Dataset:** Seoul Bike Sharing Demand
- **Official source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand)
- **Dataset ID:** 560
- **DOI:** [10.24432/C5F62R](https://doi.org/10.24432/C5F62R)
- **Number of records:** 8,760
- **Number of attributes:** 14
- **Time period:** December 1, 2017 – November 30, 2018
- **Sampling method:** The complete dataset provided by the official source was used. No additional sampling was performed.
- **Data format:** CSV
- **License:** CC BY 4.0

The dataset contains hourly bike rental counts and related information, including weather conditions, temperature, humidity, wind speed, visibility, season, and holiday status.

## Tools and Technologies

- **Python** — data retrieval, preparation, and analysis
- **Pandas** — data manipulation and CSV export
- **ucimlrepo** — retrieving the dataset from the UCI Machine Learning Repository
- **PostgreSQL** — data storage, cleaning, validation, and SQL analysis
- **SQLAlchemy** — database connection and data transfer
- **Google Colab** — executing and documenting the workflow

## Project Workflow

### 1. Data Acquisition

The dataset is retrieved directly from the UCI Machine Learning Repository using the `ucimlrepo` Python package.

The features and target data are combined into a single dataset and exported to CSV format.

### 2. Staging Table

A staging table is created in PostgreSQL to receive the raw dataset. The initial columns are stored as text to preserve the imported values before type conversion and validation.

The data is loaded using PostgreSQL's `COPY FROM STDIN` mechanism.

### 3. Data Cleaning and Type Conversion

The raw data is transformed into a structured PostgreSQL table with appropriate data types.

The process prepares the dataset for reliable querying and further analysis.

### 4. Data Quality Validation

SQL checks are performed to assess data quality and consistency, including checks for missing values, data types, and potential data integrity issues.

### 5. Exploratory Data Analysis

The notebook explores the dataset and examines bike rental demand in relation to temporal, seasonal, and weather-related variables.

The analysis helps identify patterns and potential relationships that may be useful for understanding bike-sharing demand.

## Key Results

- Successfully retrieved the complete dataset containing **8,760 hourly observations and 14 attributes**.
- Exported the retrieved data to CSV format for reproducibility and data portability.
- Implemented a PostgreSQL staging layer and bulk data-loading workflow.
- Created a structured table with appropriate data types.
- Performed data quality checks using SQL.
- Conducted exploratory analysis of rental demand and its potential relationships with weather and other factors.



The CSV file is included in the `data/` directory to make the dataset available as a separate project artifact.

## How to Run

1. Open the Jupyter notebook in Google Colab or a compatible Jupyter environment.
2. Install the required Python packages if they are not already available.
3. Retrieve the dataset from the UCI Machine Learning Repository using `ucimlrepo`.
4. Execute the notebook cells in order to reproduce the data preparation, CSV export, PostgreSQL import, validation, and analysis steps.
5. Configure a PostgreSQL connection before executing the database-related cells.

**Note:** PostgreSQL database objects and data are created in the configured database environment. They are not automatically included in the repository.

## Conclusion

This project demonstrates an end-to-end data preparation workflow combining Python and PostgreSQL. It covers data acquisition, CSV export, staging, type conversion, quality validation, and exploratory analysis, providing a reproducible foundation for further investigation of bike-sharing demand.
      
