# Covid-19 Global Impact Analysis using Power BI & SQL

## Project Overview
This project analyzes the global impact of Covid-19 from January 2020 to February 2024 using data sourced from **Our World in Data**. The dataset is ingested into **Microsoft SQL Server (MSSQL)**, transformed through **staging tables and normalization**, and visualized using **Power BI**.

## Data Sources
The following datasets were used:
1. **owid-covid-data.csv** - Contains Covid-19 cases, deaths, testing, and vaccination data.
2. **excess_mortality.csv** - Records excess mortality statistics.
3. **covid-hospitalizations.csv** - Hospitalization statistics due to Covid-19.

## Process Workflow
### 1. Data Ingestion
- CSV files are imported into **Microsoft SQL Server (MSSQL)** using **SQL Server Management Studio (SSMS)**.
- Bulk insert methods are used to load data efficiently.

### 2. Staging Tables Creation
- The raw CSV data is first ingested into **staging tables** to facilitate data cleaning and transformation.
- The `staging.sql` script contains SQL statements for creating staging tables and inserting raw data.

### 3. Data Normalization
- To improve efficiency and maintain data integrity, the staging tables are normalized.
- The `normalised table creation.sql` script restructures data into relational tables.
- Key transformations include:
  - Separating country and region details into a **location dimension table**.
  - Creating fact tables for **cases, mortality, hospitalizations, and vaccinations**.
  - Establishing relationships using **foreign keys**.

### 4. Power BI Dashboard Development
- The cleaned and structured data is imported into **Power BI**.
- The `CovidProjectUpdated.pbix` file contains:
  - **Global Trends Analysis:** Confirmed cases, recoveries, and deaths over time.
  - **Vaccination Impact:** Analysis of vaccination rates vs. Covid-19 spread.
  - **Excess Mortality:** Comparing reported Covid-19 deaths with excess mortality data.
  - **Hospitalization Trends:** Visualizing hospitalization rates by region.
- DAX measures and calculated columns are used to derive key insights.

## How to Use
1. **Database Setup:**
   - Load the CSV datasets into SQL Server.
   - Run `staging.sql` to create and populate staging tables.
   - Run `normalised table creation.sql` to create normalized tables.

2. **Power BI Visualization:**
   - Open `CovidProjectUpdated.pbix` in Power BI.
   - Ensure database connections are correctly mapped.
   - Refresh the dataset to view the latest results.

## Tools Used
- **Microsoft SQL Server (MSSQL) & SSMS** - Data storage, cleaning, and transformation.
- **SQL (T-SQL)** - Data ingestion, staging, and normalization.
- **Power BI** - Dashboard development and visualization.
- **DAX (Power BI)** - Custom calculations for insights.

## Future Enhancements
- Automate data ingestion using **Python or SQL Server Integration Services (SSIS)**.
- Implement predictive analytics for forecasting Covid-19 trends.
- Extend the dashboard to analyze socioeconomic impacts beyond health statistics.

---

**Author**: Nixon Ng  
**GitHub Repository**: [Nixonnzh](https://github.com/Nixonnzh)
