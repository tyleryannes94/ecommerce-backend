# E-Commerce Back End

## Description

This project is an e-commerce back-end application that empowers businesses to manage their online retail operations efficiently. Utilizing the latest technologies like Node.js, Express.js, Sequelize, and MySQL, this back end supports typical e-commerce functionalities including product, category, and tag management through a RESTful API. It is a demonstration of the effective use of Object-Relational Mapping (ORM) within the realm of internet retail.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Database Models](#database-models)
- [API Routes](#api-routes)
- [Demonstration Video](#demonstration-video)
- [Technologies Used](#technologies-used)
- [Repository](#repository)
- [Questions](#questions)

## Installation

To install this application, clone the repository to your local machine:

```bash
git clone https://github.com/tyleryannes94/ecommerce-backend.git 
```
Then, navigate to the directory and install the necessary dependencies:

```bash
npm install
```
To use this application, you need to have MySQL installed on your machine. Create and seed the database using the following commands:
## Create the database
```bash mysql -u root -p
source db/schema.sql
exit
```

## Seed the database
```bash
npm run seed

Start the server using: npm start
```

## Database Models
The database contains the following models:

Category: Categories for products, with fields for id (primary key, auto-incremented) and category_name.
Product: Products being sold, including fields for id, product_name, price, stock, and category_id.
Tag: Product tags for additional categorization, including fields for id and tag_name.
ProductTag: A junction model for many-to-many relationships between Product and Tag.

## API Routes
The application supports the following API routes:

GET, POST, PUT, DELETE routes for categories, products, and tags.
Routes to view all categories/products/tags or a single category/product/tag.

## Video Demo
https://www.loom.com/share/b03ec8770c9b470aaa4a294c27affcff?sid=ded12546-59da-4302-86f8-76c62d0e559e

Urls used in video:
### Products
- (GET)localhost:3001/api/products
- (GET) localhost:3001/api/products/1
- (POST) http://localhost:3001/api/products
    - json data: {"product_name": "My favorite Product", "price": 19.99, "stock": 15, "category_id": 1}
- (PUT)http://localhost:3001/api/products/1
    - json data: {"product_name": "Updated Product", "price": 29.99, "stock": 20, "category_id": 2}
(DELETE)http://localhost:3001/api/products/1

### Categories
 - (GET) localhost:3001/api/categories
 - (GET) localhost:3001/api/categories/1
 - [POST] http://localhost:3001/api/categories
    - json: {"category_name": "My favorite Category"}
- (PUT) http://localhost:3001/api/categories/2
    - json: {"category_name": "Updated Category"}
- (DELETE) http://localhost:3001/api/categories/1

### Tags
- (GET) localhost:3001/api/tags
- (GET) localhost:3001/api/tags/1
- (POST) http://localhost:3001/api/tags
    - json: {"tag_name": "Favorite Tag"}
- (DELETE) localhost:3001/api/tags/2
- (PUT) http://localhost:3001/api/tags/9
    - json: {"tag_name": "Updated to my Favorite Tag"}



## Technologies Used
Node.js
Express.js
Sequelize
MySQL
Dotenv
