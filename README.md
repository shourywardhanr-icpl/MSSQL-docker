# MSSQL Server Docker Setup

This repository contains Docker Compose configurations for setting up MSSQL Server 2017 and 2022.

## Directories

- `2022`: Contains the Docker Compose configuration for MSSQL Server 2022.
- `2017`: Contains the Docker Compose configuration for MSSQL Server 2017.

## Setup and Usage

### MSSQL Server 2022

1. Navigate to the `2022` directory:
   ```sh
   cd /home/shoury/Desktop/MSSQL/2022
   ```
2. Follow the instructions in the [2022 README](./2022/README.md).

### MSSQL Server 2017

1. Navigate to the `2017` directory:
   ```sh
   cd /home/shoury/Desktop/MSSQL/2017
   ```
2. Follow the instructions in the [2017 README](./2017/README.md).

## Common Commands

- To start the MSSQL Server container:
  ```sh
  docker-compose up -d
  ```
- To stop the MSSQL Server container:
  ```sh
  docker-compose down
  ```

Ensure you have Docker installed on your machine before running the commands.
