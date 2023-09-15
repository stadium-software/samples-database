# Samples Database

A number of the samples require this database

## Version

1.0

## Database

Create the MSSQL database by running the SQL script in the Database folder of this repo 

## Connector

1. Add a Database connector to the Database you created in the step above 
2. Add a query to select the data for the DataGrid
```
select * from MyData
```

## DataGrid

1. Add a DataGrid Control to a page
2. Define DataGrid columns in the *Columns* property of the DataGrid
3. Open the StartPage.load event handler
4. Drag the query in the StartPage.Load event handler of the page
5. Drag a SetValue function under the query in the StartPage.load event handler
6. Assign the data returned by the query to the DataGrid

