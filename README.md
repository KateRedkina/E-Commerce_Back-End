# E-Commerce_Back-End

## Description

This application was created as part of a Full Stack Coding Bootcamp challenge. Given the starter code of a working Express.js API, code was configured to use Sequelize to interact with a MySQL database. 

Code syncs Sequelize models to a MySQL database on the server start, includes column definitions for all four models and model associations, and provides the following GET, POST, PUT, and DELETE routes:

**Category**
 * GET all categories, GET a single category by ID, POST(create) a new category, PUT(update) an existing category by ID, and DELETE an existing category by ID. 

**Tag**
 * GET all tags, GET a single tag by ID, POST(create) a new tag, PUT(update) an existing tag by ID, and DELETE an existing tag by ID.

**Product (including ProductTag)**
 * GET all products, GET products by ID, and DELETE products by ID. POST(create) and PUT(update) an existing product by ID .

**Watch [video](https://drive.google.com/file/d/1eYG7Cm0h8bG9MRZt9c2PAgpVknfcWFZ8/view) to see demonstration of all API routes' endpoints using Insomnia:**

## Installation
* Check if you have Node.js installed by typing `node -v` in your command line. If node is not installed, visit the [Node.js](https://nodejs.org/en) website to install. 
* Next, clone this project repository to your computer. 
* Use the command `npm i` to install dependencies. 
* Create a file in the root directory titled `.env` and include database name and personal MySQL login information:
```
DB_NAME='ecommerce_db'
DB_USER='YOUR USERNAME'
DB_PASSWORD='YOUR PASSWORD'
```
* Open MySQL with command `mysql -u root -p` and enter your personal MySQL password. 
* Create databse with command `source db/schema.sql`. Log out of MySQL with command `\q`.
* Seed database with command `npm run seed`.

## Usage
* Start server with command `npm start`.
* Access API routes with Insomnia using the following endpoints:

|                                   | CATEGORY                                 | TAG                                | PRODUCT                                |
|-----------------------------------|------------------------------------------|------------------------------------|----------------------------------------|
| GET (ALL), POST(CREATE)           | http://localhost:3001/api/categories/    | http://localhost:3001/api/tags/    | http://localhost:3001/api/products/    |
| GET (BY ID), PUT(UPDATE),  DELETE | http://localhost:3001/api/categories/:id | http://localhost:3001/api/tags/:id | http://localhost:3001/api/products/:id |


* Make POST and PUT requests with the following JSON body formats:

 **CATEGORY**
  ```
  { 
  "categoryName": "STRING INPUT" 
  }
  ```
 **TAG**
  ```
  { 
  "tagName": "STRING INPUT" 
  }
  ```
  **PRODUCT**
  ```
  { 
  "product_name": "STRING INPUT",   
  "price": DECIMAL INPUT,   
  "stock": INTEGER INPUT,   
  "tagIds": INTEGER INPUT
  }
  ```
## License

[MIT License](https://opensource.org/licenses/MIT)

## Links
* GithHub repository: https://github.com/KateRedkina/E-Commerce_Back-End