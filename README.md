# 13-Object-Relational-Mapping-ORM-E-Commerce-Back-End
# 13 Object-Relational Mapping (ORM): E-Commerce Back End

## My Task
My task is to build the back end for an e-commerce site by modifying starter code. I’ll configure a working Express.js API to use Sequelize to interact with a MySQL database.


Database Models
* Category
    * id
        * Integer
        * Doesn't allow null values
        * Set as primary key
        * Uses auto increment
    * category_name
        * String
        * Doesn't allow null values
* Product
    * id
        * Integer
        * Doesn't allow null values
        * Set as primary key
        * Uses auto increment
    * product_name
        * String
        * Doesn't allow null values
    * price
        * Decimal
        * Doesn't allow null values
        * Validates that the value is a decimal
    * stock
        * Integer
        * Doesn't allow null values
        * Set a default value of 10
        * Validates that the value is numeric
    * category_id
        * Integer
        * References the category model's id
* Tag
    * id
        * Integer
        * Doesn't allow null values
        * Set as primary key
        * Uses auto increment
    * tag_name
        * String
* ProductTag
    * id
        * Integer
        * Doesn't allow null values
        * Set as primary key
        * Uses auto increment
    * product_id
        * Integer
        * References the product model's id
    * tag_id
        * Integer
        * References the tag model's id
        * 

Data Associations
You'll need to execute association methods on your Sequelize models to create the following relationships between them:
* Product belongs to Category, as a category can have multiple products but a product can only belong to one category.
* Category has many Product models.
* Product belongs to many Tag models. Using the ProductTag through model, allow products to have multiple tags and tags to have many products.
* Tag belongs to many Product models.
