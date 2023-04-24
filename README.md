# Oracle Recipe #3: How to Execute a query that returns a Single Row with the method GetOracleValues

if you want to obtain multiple values from a database, you can call the executeReader method once on a OracleCommand object, to execute a SQL statement that returns a collection of values in a single row result.

The ExecuteReader method returns an instance of a class that implements the IDataReader interface. Each of the data reader classes provided by .NET Framework has a GetValues method, which returns an array of column values for the current row.

To obtain a single row from a database.
Open a OracleConnection.
Create and initialize a OracleCommand object.
Call the ExecuteReader method on the command object. Assign the return value from this method to a data reader variable.
Call the Read method on the data reader object to move to the first(and only) row in the result set.
Call the GetOracleValues method on the data reader object. Pass an object array as a parameter to retrieve the scalar results of the query.
Convert each element in the array to an appropriate data type, if necessary.
Close the OracleDataReader object.
Dispose the OracleCommand object.
Close the database connection.
The following example shows how to execute a query that returns a set of values. The example place the results into an array named results.

Fig 1. Using the GetOracleValues of an OracleDataReader object.

OracleDataReader GetOracleValues method code example

Download example source code.
