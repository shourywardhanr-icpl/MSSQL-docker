# MSSQL Server 2017 Usage Guide

## Connecting to the Database

You can connect to the MSSQL Server using various tools such as SQL Server Management Studio (SSMS), Azure Data Studio, or the `sqlcmd` utility.

### Using SQL Server Management Studio (SSMS)

1. Open SSMS.
2. In the "Connect to Server" dialog, enter the following details:
   - **Server name:** `localhost,1433`
   - **Authentication:** SQL Server Authentication
   - **Login:** `sa`
   - **Password:** `Anubhav@321`
3. Click "Connect".

### Using Azure Data Studio

1. Open Azure Data Studio.
2. Click on "New Connection".
3. Enter the following details:
   - **Server name:** `localhost`
   - **Authentication Type:** SQL Login
   - **User name:** `sa`
   - **Password:** `Anubhav@321`
4. Click "Connect".

### Using `sqlcmd`

1. Open a terminal.
2. Run the following command:
   ```sh
   sqlcmd -S localhost -U sa -P "Anubhav@321"
   ```

## Running SQL Queries

Once connected, you can run SQL queries to interact with the database.

### Example Queries

- **Create a new database:**
  ```sql
  CREATE DATABASE TestDB;
  ```

- **Create a new table:**
  ```sql
  USE TestDB;
  CREATE TABLE Users (
      ID INT PRIMARY KEY,
      Name NVARCHAR(50),
      Email NVARCHAR(50)
  );
  ```

- **Insert data into the table:**
  ```sql
  INSERT INTO Users (ID, Name, Email) VALUES (1, 'John Doe', 'john.doe@example.com');
  ```

- **Select data from the table:**
  ```sql
  SELECT * FROM Users;
  ```

## Backup and Restore

### Backup a Database

1. Connect to the server using any of the methods mentioned above.
2. Run the following SQL command:
   ```sql
   BACKUP DATABASE TestDB TO DISK = '/var/opt/mssql/backup/TestDB.bak';
   ```

### Restore a Database

1. Connect to the server using any of the methods mentioned above.
2. Run the following SQL command:
   ```sql
   RESTORE DATABASE TestDB FROM DISK = '/var/opt/mssql/backup/TestDB.bak';
   ```

## Additional Resources

- [SQL Server Documentation](https://docs.microsoft.com/en-us/sql/sql-server/)
- [SQL Server Tutorials](https://docs.microsoft.com/en-us/sql/sql-server/tutorials/)
