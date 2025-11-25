# ETLSales

Read before start :

This project demonstrates an ETL process using SSIS .

Tools Used
-----------

SSMS (SQL Server Management Studio)

SSIS (SQL Server Integration Services, via Visual Studio)


Getting Started (with Fact/Dim tables)
---------------------------------------
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




Getting Started with Normalization
-----------------------------------
1. Set Up the Database
-----------------------

A source database (datalake) already exists.
To create the Normalization database in SQL Server Management Studio (SSMS):

Navigate to the queries folder in this repository.

Open the normalization.txt file.

Run the script in SSMS to create the Normalization database.

2. Configure SSIS Parameters
------------------------------

This project uses two parameters in SSIS:

DatalakeName – the name of your existing datalake database

NormalizationDBName – the name of your new Normalization database

Update these parameters to match the database names you created in your environment.



