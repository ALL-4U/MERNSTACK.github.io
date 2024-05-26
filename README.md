# MERN Stack Coding Challenge

## Overview

This coding challenge involves creating a full-stack MERN (MongoDB, Express, React, Node.js) application that interacts with a third-party API to fetch transaction data, initializes a database, and provides several APIs for data manipulation and visualization. The frontend will use these APIs to display the data in tables and charts.

## Project Structure

### Backend

#### Data Source

- **Third Party API URL**: `https://s3.amazonaws.com/roxiler.com/product_transaction.json`
- **Request Method**: GET
- **Response Format**: JSON

#### API Endpoints

1. **Initialize Database**
   - **Endpoint**: `/api/init`
   - **Method**: GET
   - **Description**: Fetches JSON data from the third-party API and initializes the database with seed data.

2. **List Transactions**
   - **Endpoint**: `/api/transactions`
   - **Method**: GET
   - **Description**: Lists all transactions with support for search and pagination.
   - **Query Parameters**:
     - `month` (required)
     - `search` (optional)
     - `page` (default: 1)
     - `perPage` (default: 10)

3. **Statistics**
   - **Endpoint**: `/api/statistics`
   - **Method**: GET
   - **Description**: Provides statistics for the selected month.
   - **Query Parameters**:
     - `month` (required)

4. **Bar Chart Data**
   - **Endpoint**: `/api/barchart`
   - **Method**: GET
   - **Description**: Provides data for a bar chart based on price ranges for the selected month.
   - **Query Parameters**:
     - `month` (required)

5. **Pie Chart Data**
   - **Endpoint**: `/api/piechart`
   - **Method**: GET
   - **Description**: Provides data for a pie chart with unique categories and item counts for the selected month.
   - **Query Parameters**:
     - `month` (required)

6. **Combined Data**
   - **Endpoint**: `/api/combined`
   - **Method**: GET
   - **Description**: Fetches and combines data from the statistics, bar chart, and pie chart APIs.
   - **Query Parameters**:
     - `month` (required)

### Frontend

#### Features

1. **Transactions Table**
   - Lists transactions based on the selected month.
   - Includes a search box to filter transactions by title, description, or price.
   - Supports pagination with "Next" and "Previous" buttons.

2. **Transactions Statistics**
   - Displays total sale amount, total sold items, and total unsold items for the selected month.

3. **Transactions Bar Chart**
   - Displays a bar chart with price ranges and the number of items in each range for the selected month.

4. **Transactions Pie Chart**
   - Displays a pie chart with unique categories and item counts for the selected month.

#### User Interface

- **Month Dropdown**: Allows users to select a month from January to December.
- **Default Selection**: March is selected by default.
- **Search Box**: Filters transactions based on the input text.
- **Pagination**: "Next" and "Previous" buttons navigate through pages of transactions.

## Setup Instructions

### Prerequisites

- Node.js and npm installed on your system
- MongoDB installed and running

### Backend Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/ShivanshTiwari01/Roxiler-Systems-Coding-Challenge
   cd  Roxiler-Systems-Coding-Challenge/backend

2. Install dependencies

    npm install

3. Run the server

    npm start


### Frontend Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/ShivanshTiwari01/Roxiler-Systems-Coding-Challenge
   cd  Roxiler-Systems-Coding-Challenge/frontend

2. Install dependencies

    npm install

3. Run the server

    npm start


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
