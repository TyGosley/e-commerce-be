# E-commerce:  Back End

## Table of Contents

___

* [Description](#description)
* [Languages](#languages)
* [Installation](#installation)
* [Routes](#routes)
* [Demonstration](#demonstration)
* [Questions](#questions)
* [Credits](#credits)
* [Licenses](#licenses)

## Description

___
As a manager at an internet retail company, you want a back end for your e-commerce website that uses the latest technologies so that you can compete with other e-commerce companies. With this application, you can use Object-Relational Mapping (ORM) and the E-commerce(back end) will help you with the following:

* Access all products along with their categories and tags
* Access categories along with their associated products
* Access tags along with their associated products
* Add new products, categories, and tags
* Update a product's tags, a category name, and tag names
* Delete any product, category, or tag

## Languages

___
This application was built using:

* Sequelize
* MySQL2
* Node/NPM
* Express.js
* Dotenv
* JavaScript

## Installation

___

1. **Copy Link:** Hit the "Code" button within this GitHub repo to copy link.

2. **Clone:** Use the command "git clone *paste link here*".

3. **NPM:** Run the command **npm install** or **npm i** to install Node Package Manager and dependencies.

4. **Dotenv:** In your root folder, make sure to create a .env file with the following information:

  * DB_NAME='ecommerce_db'
  * DB_USER='*your mysql username*'
  * DB_PW='*your mysql password*'  

  Your MySQL login information will then be passed to config/connection.js. This is necessary to sync the Sequelize models to the MySQL database on server start. This keeps your password hidden and can prevent hacking down the line.  This is good practice.

5. **MySql:** Using MySQL shell command line, run the command **source db/schema.sql** to download the database to your remote workspace.

6. **Seeds:** Using the repository's integrated terminal, run the command **npm run seed** or **node seeds/index.js** to seed existing data to the database.

7. **Connect to Server**: Once the previous installation instructions are complete, use your integrated terminal to start the server with **npm start** or **node server.js.**

8. Remember to download and install [Insomnia](https://insomnia.rest/download). It is free and is a great resource to help with this applications and many others like it.

## Routes

___
Navigate to Insomnia Core. Use the base link http://localhost:3001/api/*given spec*

Given specifications are outlined below.

Example: to GET the product with an id of 1, add the 'products/*product id*' endpoint from the GET (one) category to the end of the base link:  

http://localhost:3001/api/categories/2 

Run in Insomnia using the 'GET' route.

**GET (all):**

* products:  example (localhost:3001/api/products) 

* categories:  example (localhost:3001/api/categories)
* tags:  example (localhost:3001/api/tags)

**GET (one):**

* products/*product id*:  example (localhost:3001/api/product/1)

* categories/*category id*:  example (localhost:3001/api/categories/1)

* tags/*tag id*:  example (localhost:3001/api/tags/1)

**POST: (Example)** 

* products  
JSON:  
{  
  "product_name": "*best product ever*",  
  "price": *10.99*,  
  "stock": *25*,  
  "tagIds": [*array of some integers*]  
}

* categories  
JSON:  
{  
  "category_name": "*some string*"  
}

* tags  
JSON:  
{  
  "tag_name": "*some string*"  
}

**Use the previous examples with different CRUD 
operations**

**PUT:**

* products/*product id*  
JSON:  
{  
  "tagIds": [*array of some integers*]  
}

* categories/*category id*  
JSON:  
{  
  "category_name": "*some string*"  
}

* tags/*category id*  
JSON:  
{  
  "tag_name": "*some string*"  
}

**DELETE:**

* products/*product id*  
* categories/*category id* (see note below)  
* tags/*category id*

NOTE: Categories for products cannot be null! When running delete categories route, only delete categories that do not have associated products. To accomplish this, delete a category after using a POST route to create one.

## Demonstration

___
Would you like to see E-commerce back-end in action?

Watch this [demo]().

## Questions

___

Have questions about this project?  

GitHub: https://github.com/TyGosley 

Email: tygosley@gmail.com

## Credits

___

Starter Code: Database, seeds, & dependencies: UCLA Extenstion: Full Stack Web Developing Bootcamp

[NPM](https://docs.npmjs.com/)

[Sequelize](https://sequelize.org/docs/v6/getting-started/)

[Codecademy](https://www.codecademy.com/learn)

[Khan Academy](https://www.khanacademy.org/)

[MDN Docs](https://developer.mozilla.org/en-US/)

[W3Schools](https://www.w3schools.com/js/default.asp)

[JavaScript.info](https://javascript.info/)

[CodeHS](https://codehs.com/)

## Licenses

___

N/A