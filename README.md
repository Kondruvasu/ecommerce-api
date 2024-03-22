
Ecommerce Platform Admin API
This project aims to design a RESTful API for managing product inventory for an ecommerce platform. The API is built using Node.js and MongoDB, providing endpoints to perform CRUD (Create, Read, Update, Delete) operations on product data.

Tech Stack:-
Node.js
MongoDB
Postman for API testing
Getting Started
To get started with the project, follow these steps:

Clone the repository:-

bash

git clone <repository_url>
Install dependencies:


npm install
Set up MongoDB:-

Make sure you have MongoDB installed and running locally or update the MongoDB connection string in the project's configuration file.
Start the server:

sql
npm start
Models/Schemas
The project includes the following model/schema:

Products
Fields: id, name, quantity
API Endpoints
1. Add Products
URL: POST /products/create
Request Body:
json

{
  "product": {
    "name": "laptop",
    "quantity": 10
  }
}
Response:
json
Copy code
{
  "data": {
    "product": {
      "name": "laptop",
      "quantity": 10
    }
  }
}
2. List Products
URL: GET /products
Response:
json
{
  "data": {
    "products": [
      {
        "id": 1,
        "name": "laptop",
        "quantity": 10
      },
      {
        "id": 2,
        "name": "camera",
        "quantity": 5
      },
      {
        "id": 3,
        "name": "smartwatch",
        "quantity": 8
      }
    ]
  }
}

3. Delete Products
URL: DELETE /products/:id
Response:
json
Copy code
{
  "data": {
    "message": "product deleted"
  }
}
4. Update Product Quantity
URL: POST /products/:id/update_quantity/?number=10
Response:
json
Copy code
{
  "data": {
    "product": {
      "id": 1,
      "name": "laptop",
      "quantity": 20
    },
    "message": "updated successfully"
  }
}
Testing
Use Postman or any other API testing tool to test the endpoints. Make sure to send requests with the correct method and payload as described above.
