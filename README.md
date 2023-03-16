# StoreAPI

In this project I ceated an API for a store. It allows the user to search for products with a name that contains their search value in at least part of it. It allows users to utilize pages and limit the number of products that are displayed on each page. Users can utilize categorical searches as well as apply Numeric filters to fields like price and rating. Finally it allows users to specify which fields they want to receive from the API as well as sort them.

# API Documentation

## Fields and their validations

* name:
- type: String
- required

* price:
- type: Number
- required

* featured:
- type: Boolean
- default: false

* rating:
- type: Number
- default: 4.5

* createdAt:
- type: Date
- default: Current Date

* company:
- type: String
- must be one of ("ikea", "liddy", 'caressa', 'marcos')


## Get Requests Available:

* Get an array of all the products in the API:
- Example: http://localhost:3000/api/v1/products

* Sort elements:
- Example: http://localhost:3000/api/v1/products?sort=price
- This will sort all product in the array from the lowest price to the highest price
- Including '-' infront of field from highest tolowest in Integers | DESC Alphabetical form

* Receive elements with specific fields:
- Example: http://localhost:3000/api/v1/products?fields=price
- This will return only the name of the elements 

* Receive elements with specific name:
- Example: http://localhost:3000/api/v1/products?name=wooden desk
- This will return the product with the name "wooden desk"

* Receive elements wich include specific name:
- Example: http://localhost:3000/api/v1/products?name=desk
- This will return the product with "desk" included in their name

* Receive elements on specific page:
- Example: http://localhost:3000/api/v1/products?page=3,limit=10
- This will return elements on page 3, the number of elements displayed on each page would be 10


## What I Learned

* I learnt how to use express-async-errors to handle errors
* I learnt how to sort elements dynamically in a request
* I learnt how to receive specific fields dyanmically in a request
* I learnt how to provide page functionality in an API
* I learnt how to provide elements in an API based on only part of their names
* I learnt how to apply numeric filtration in an API request


## Dependencies 

* "body-parser": "^1.20.2",
* "dotenv": "^8.2.0",
* "express": "^4.17.1",
* "mongoose": "^5.11.10"
* "nodemon": "^2.0.7"
* "express-async-errors": "^3.1.1"
