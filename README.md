# ETL_and_PowerBI_Sales

Read before start :

This project demonstrates an ETL process using SSIS and the creation of a Power BI dashboard for sales data.

Tools Used
-----------

SSMS (SQL Server Management Studio)

SSIS (SQL Server Integration Services, via Visual Studio)

Power BI

Getting Started
----------------
Step 1: Set Up Databases
-------------------------

Create two databases:

1-DataLake: Stores raw data without any transformations or cleaning.

2-DataWarehouse: Stores cleaned and structured data for analytics.

Import Data :
Import the Excel files provided in the repository into the DataLake database.

Step 2: Prepare the Data Warehouse
-----------------------------------
Create tables as specified in the text document included in the repository.

These tables are split into Fact and Dimension tables for efficient analytics.

Fact tables store transactional data, and Dimension tables store descriptive data .

Step 3: Configure the SSIS Project
-----------------------------------

1-Update Parameters

Before running the SSIS project, set the database names (DataLake and DataWarehouse) in the project parameters.

2-Enable Currency Component

By default, the currency component is disabled.

To enable it:

Open the component’s C# script in the SSIS project.

Add your API key from "https://www.exchangerate-api.com/" (free API).

save then enable it 

Step 4: Run the ETL Process
-----------------------------

After configuring the parameters and enabling the currency component, execute the SSIS package to move and transform the data from the DataLake to the DataWarehouse.
