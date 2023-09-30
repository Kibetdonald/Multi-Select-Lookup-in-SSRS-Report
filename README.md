# Multi-Select-Lookup-in-SSRS-Report
This project demonstrates how to create a multi-select lookup in an SQL Server Reporting Services (SSRS) report. The goal is to allow users to select multiple items from a lookup, enhancing the interactivity and usability of your SSRS reports.

## Components
1. SalesOrderContractClass
  - This class defines the contract for the report.
  - It includes a list variable customerAcc to store customer account numbers.
  - The parmCustomerAccount method is used to get and set the customer account list.
2. SalesOrderUIBuilder
  - This class is responsible for building the user interface (UI) for the report parameters.
  - It includes a method ItemIdLookup for performing lookups on customer account numbers.
  - The build method sets up the UI, and the postBuild method handles UI-related tasks.
  - The postRun method can be used for additional post-processing.
3. SalesOrderDPClass
  - This class acts as the data provider for the report.
  - It retrieves data from the database based on the selected customer accounts.
  - The getSalesOrderTmp method fetches data from the SalesOrderTmp table.
  - The processReport method processes the data and inserts it into the report dataset.
