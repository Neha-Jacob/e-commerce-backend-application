# A Basic Product Catalog and Shopping Cart Service

## Overview

Create the following tables and expose an API for CRUD (Create, Retrieve, Update, Delete) operations to be used by internal users. Authentication is not required. Database: PostgreSQL or MySQL. The SQL file should be properly versioned in Git:

- **Product Master**
  - Name
  - Specification (key/value)
  - SKU
  - Category
  - Price

- **Category Master**
  - Name

- **Inventory**
  - Product
  - Quantity

The SQL file should be properly versioned in Git.

If there is any update in the schema, the developer should update the SQL in such a way that one does not have to delete the database and recreate it again. (Optional)

## Develop a Product Catalog Service

- **GetProducts**
  - Should return all products with minimum detail.
  - Return a maximum of 20 products at a time and use pagination.

- **GetProduct**
  - Should return product details.

## Develop an Add To Cart Service

- Prepare the data model (types) such that a proper relationship can be presented between product, inventory, and cart.

- **AddItemToCart**
  - Should be able to add selected products and quantities to a cart.
    - If there is not enough quantity, return an error with an appropriate message.
  - Save the cart in the database.
  - Design the tables so that they can store information about the cart and its items.
  - Return a cart reference, items in the cart, and the total cart value.

- **AddItemsToCart**
  - Should add multiple items and their quantities to the cart and return the response as mentioned above.

## API Exposure

Expose APIs for all these operations so that one can use Postman or similar tools to interact.

## Console Interface

Develop a console interface to interact with the system.

- The user should be able to perform the CRUD operations mentioned above.

## Application Development

- Develop the application with proper separation of logic so that a UI can be developed later to interact with the system.
- Systematically log errors (logical, runtime, validation) to a file.
- Add sufficient unit tests. 
