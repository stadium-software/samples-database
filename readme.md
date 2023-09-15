# Samples Database

A number of the samples require this database

## Version

1.0

## Database

Create a MSSQL database called "StadiumFilterData" by running the SQL script called filterdata.sql in this repo 

## Connector
Add a Database connector in the Stadium Designer

1. Click on the *Connectors* button in the toolbar and selecting *Database* in the dropdown
2. Enter the connection details in the popup window
   1. Server name
   2. Username
   3. Password
   4. Database
3. Check the "Trust Server Certificate" checkbox

## Query
Add a query to select the data for the DataGrid

1. Click the plus icon next to the connector to add a query
2. Name the query as you see fit
3. Right-click on the table called "MyData" in the main tab
4. Select "Generate Select" or copy and paste the SQL below into the *Query* tab
```
SELECT ID
      ,FirstName
      ,LastName
      ,NoOfChildren
      ,NoOfPets
      ,StartDate
      ,EndDate
      ,Healthy
      ,Happy
      ,Subscription
  FROM dbo.MyData;
```
5. Click the *Fetch Fields & Parameters* button 

## DataGrid

1. Add a DataGrid Control to a page
2. Define DataGrid columns in the *Columns* property of the DataGrid
3. Open the StartPage.load event handler
4. Drag the query in the StartPage.Load event handler of the page
5. Drag a SetValue function under the query in the StartPage.load event handler
6. Assign the data returned by the query to the DataGrid
