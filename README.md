# API FOR CATEGORIES AND PRODUCTS
This api it's a crud for registry categories and products of a ecommerce

## Endpoints

### GET /category
A endpoint for return all categories registered
#### Params
Empty!

#### Response
##### OK! 200
Exemple of response:
```
[
    {
        "id": 37,
        "name": "Category Exemple"
    }
]
```
if you receive a OK yours categories will be listed

##### Internal Server Error! 500
If you take a error in your listing, the code will return for your the error catched by the code and a internal server error.

### GET /category/ID
This endpoint will take for you a category by id.

### Params
Send in URL the id of desired category
```
http://localhost:8080/category/37
```
#### Response
##### OK! 200
Exemple of response:
```
[
    {
        "id": 37,
        "name": "Category Exemple"
    }
]
```
##### Bad Request! 400
```
{
    "err": "id is required"
}
```
If you don't send the id in request.

### POST /category
Endpoint for register yours categories
#### Params
```
{
    "name": "Category Exemple"
}
```
#### Response
##### OK! 200
``` 
{
     "name": "Category Exemple"
}
```
##### Bad Request! 400
```
{
    "err": "err"
}
```
if you take a error in in decoding your request.

##### Internal Server Error! 500
If you take a error in your inserting, the code will return for your the error catched by the code and a internal server error.

### GET /product
A endpoint for return all products registered

#### Params
Empty!

#### Response
##### OK! 200
Exemple of response:
```
[
    {
        "id": 567,
        "name": "Product Exemple",
        "description": "product description will here",
        "category_id": 37,
        "image_url": "https://www.imageurl.com/asdfasdfasdf"
        "price": 17,30
    },
    {
        "id": 734,
        "name": "Product Exemple",
        "description": "product description will here",
        "category_id": 37,
        "image_url": "https://www.imageurl.com/asdfasdfasdf"
        "price": 16,30
    }
    
]
```
if you receive a OK yours products will be listed

##### Internal Server Error! 500
If you take a error in your listing, the code will return for your the error catched by the code and a internal server error.

### GET /product/ID
This endpoint will take for you a product by id.

### Params
Send in URL the id of desired product
```
http://localhost:8080/product/734
```
#### Response
##### OK! 200
Exemple of response:
```
[
    {
        "id": 734,
        "name": "Product Exemple",
        "description": "product description will here",
        "category_id": 37,
        "image_url": "https://www.imageurl.com/asdfasdfasdf"
        "price": 16,30
    }
]
```
##### Bad Request! 400
```
{
    "err": "id is required"
}
```
If you don't send the id in request.

##### Internal Server Error! 500
If you take a error in your listing, the code will return for your the error catched by the code and a internal server error.

### GET /product/category/ID
This endpoint will take for you the products by category id.

### Params
Send in URL the id of desired category that you want to list
```
http://localhost:8080/product/category/37
```
#### Response
##### OK! 200
Exemple of response:
```
[
    {
        "id": 567,
        "name": "Product Exemple",
        "description": "product description will here",
        "category_id": 37,
        "image_url": "https://www.imageurl.com/asdfasdfasdf"
        "price": 17,30
    },
    {
        "id": 734,
        "name": "Product Exemple",
        "description": "product description will here",
        "category_id": 37,
        "image_url": "https://www.imageurl.com/asdfasdfasdf"
        "price": 16,30
    }
    
]
```
##### Bad Request! 400
```
{
    "err": "categoryId is required"
}
```
If you don't send the id in request.

##### Internal Server Error! 500
If you take a error in your listing, the code will return for your the error catched by the code and a internal server error.

### POST /product
Endpoint for register yours products
#### Params
```
{
        "id": 567,
        "name": "Product Exemple",
        "description": "product description will here",
        "category_id": 37,
        "image_url": "https://www.imageurl.com/asdfasdfasdf"
        "price": 17,30
}
```
#### Response
##### OK! 200
``` 
{
        "id": 567,
        "name": "Product Exemple",
        "description": "product description will here",
        "category_id": 37,
        "image_url": "https://www.imageurl.com/asdfasdfasdf"
        "price": 17,30
}
```
##### Bad Request! 400
```
{
    "err": "err"
}
```
if you take a error in in decoding your request.

##### Internal Server Error! 500
If you take a error in your insert, the code will return for your the error catched by the code and a internal server error.
