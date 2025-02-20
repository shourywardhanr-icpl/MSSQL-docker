# MSSQL Server 2017 Docker Setup

## Setup

1. Ensure you have Docker installed on your machine.
2. Navigate to the `2017` directory:
   ```sh
   cd /home/shoury/Desktop/MSSQL/2017
   ```
3. Start the MSSQL Server container:
   ```sh
   docker-compose up -d
   ```

## Usage

- To connect to the MSSQL Server, use the following credentials:
  - **Username:** `sa`
  - **Password:** `Anubhav@321`
- The server will be accessible on port `1433`.

## Health Check

- The container includes a health check that runs every 10 seconds to ensure the server is running.

## Stopping the Server

- To stop the MSSQL Server container, run:
  ```sh
  docker-compose down
  ```
