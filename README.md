# Bike-Crash-Data-Analysis-using-BI

## Repository Description:
This repository contains the complete data pipeline and analysis process for bike crash records from Chicago, Austin and New York cities. The project includes data profiling, data modeling, staging, ETL processes, and insights generation, implemented using SQL Server, SSMS, and various data transformation tools.

# Table of Contents
1. Project Overview
2. Technologies Used
3. Data Pipeline
  a. Data Profiling
  b. Dimensional Modeling
  c. Staging Tables
4. Setup and Installation
5. Usage
6. Contributors
7. License

# Project Overview
This project analyzes bike crash datasets from three cities: Chicago, New York and Austin. The analysis includes detailed data profiling, anomaly handling, and staging. A dimensional data model was created to facilitate querying and analysis for food safety violations, risk assessments, and inspection results.

## Key aspects of the project:

1. **Data Sources**: Food inspection data from Chicago and Dallas
2. **ETL Process**: Data profiling, cleaning, dimensional modeling, and loading into staging tables for analysis
3. **Output**: Detailed reports and insights based on the data, including violations, risk categories, and inspection results
# Technologies Used
1. **Database**: Microsoft SQL Server (SSMS)
2. **ETL Tools**: TMap, Bash Scripts, Advanced Excel Techniques
3. **Reporting Tools**: Tableau, Power BI
4. **Languages**: SQL, Bash, Excel Macros
5. **Collaboration & Version Contro**l: Git, GitHub

Note: To access Power BI file visit https://app.powerbi.com/groups/me/reports/7bf84b8a-86a1-453e-b536-e3f07e2b136f/ReportSection?experience=power-bi

# Data Pipeline
## Data Profiling
Data profiling was performed to ensure data quality and identify anomalies. We utilized y-data profiling to analyze the structure of the datasets for both cities, as detailed in the profiling reports:

**Chicago Dataset**: 2,067,603 records, 30 fields
**New York Dataset**: Analysis performed with a focus on violations, risk categories, and facility types​.
**Austin Dataset**: 2,367,068 records, 45 fields

# Dimensional Modeling
The data was structured using a dimensional model to support efficient querying and reporting. Key dimensions include:

**Dim_Business**: Business-related information (DBA Name, License, etc.)
**Dim_**: Facility type information (Restaurant, Grocery Store, etc.)
**Dim_Violations**: Results of inspections (Pass, Fail, etc.)
**Dim_Location**: Location data (Address, City, State, Zip, Latitude, Longitude)
**Fact Tables**: Fact_Inspection and Fact_Violations were built using the normalized dimensions​.
## Staging Tables
Data was loaded into staging tables for all cities (Chicago and New York and Austin). Anomalies such as multiline values were handled during this process. Staging steps included splitting violation data into individual columns and handling location-based data transformations​(Food Inspection PART 3).

# Setup and Installation
To run this project locally:

1. Clone this repository:
bash
Copy code
git clone https://github.com/yourusername/food-inspection-analysis.git
cd food-inspection-analysis
2. Ensure you have SQL Server and SSMS installed. The required DDL scripts for setting up staging tables are located in the /scripts folder.
3. Load the provided datasets into the staging tables using the ETL scripts included.
4. Use the Tableau or Power BI dashboards to visualize the results.
# Usage
1. Run the provided SQL scripts to load data into staging tables.
2. Use the ETL_Transformations.sql script to perform data transformations.
3. Generate reports using Tableau or Power BI by connecting to the SQL Server database and following the report templates provided.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

