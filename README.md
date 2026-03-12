# Store Management Backend API

A complete backend solution for managing a store's product inventory, built using Node.js, Express, and MongoDB.

## Features
- Full CRUD operations for Products
- Filter products by category
- Search products by name
- Strict validation rules using Mongoose Schema
- Global Error Handling
- Ready to deploy to Render

## Tech Stack
- **Node.js**: JavaSript Runtime Environment
- **Express.js**: Web Framework for Node
- **MongoDB & Mongoose**: NoSQL Database and Relational Object Mapping
- **dotenv**: Environment Management Environment Setup

## Requirements

Before starting ensure you have these installed:
- Node.js (v14 or higher)
- MongoDB Database (either Local or an Atlas Cluster URI)

## Installation & Setup

1. **Install dependencies:**
    ```bash
    npm install
    ```

2. **Environment Variables Configuration:**

    Create a file called `.env` in the root and configure these variables:
    ```
    PORT=5000
    MONGO_URI=your_mongodb_connection_string
    ```

3. **Run the Server:**
    ```bash
    npm start
    ```
    The server will start listening on port 5000: `http://localhost:5000`

## API Endpoints Overview

Test these endpoints locally or on production through tools like Postman. 

- **Create a Product**
  - **Method**: `POST`
  - **Path**: `/products`
  - **Body (JSON)**:
    ```json
    {
       "name": "Sony Headphones",
       "productCode": "SN-001",
       "supplierName": "Sony Electronics",
       "quantityInStock": 50,
       "unitPrice": 120,
       "reorderLevel": 10,
       "category": "Electronics",
       "productType": "Non-Perishable"
    }
    ```

- **Get all Products**
  - **Method**: `GET`
  - **Path**: `/products`

- **Get a Product by ID**
  - **Method**: `GET`
  - **Path**: `/products/:id`

- **Update a Product**
  - **Method**: `PUT`
  - **Path**: `/products/:id`

- **Delete a Product**
  - **Method**: `DELETE`
  - **Path**: `/products/:id`

- **Search Product by Name**
  - **Method**: `GET`
  - **Path**: `/products/search?name=Sony`

- **Filter Product by Category**
  - **Method**: `GET`
  - **Path**: `/products/category?cat=Electronics`

## Deployment Recommendations (Render)

1. Connect your repository to Render using a New Web Service.
2. Ensure you provide `npm install` as the install command.
3. Ensure you provide `npm start` as the start command.
4. From the Render Dashboard, add the `PORT` (e.g., `5000`) and the `MONGO_URI` strings within the Environment Variables settings.
