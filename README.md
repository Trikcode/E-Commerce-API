
# E-commerce-API



<!--- If we have only one group/collection, then no need for the "ungrouped" heading -->



## Endpoints

* [Auth](#auth)
    1. [RegisterUser](#1-registeruser)
    1. [LoginUser](#2-loginuser)
    1. [LogoutUser](#3-logoutuser)
* [User](#user)
    1. [GetAllUsers](#1-getallusers)
    1. [ShowCurrentUser](#2-showcurrentuser)
    1. [UpdateUser](#3-updateuser)
    1. [UpdateUserPassword](#4-updateuserpassword)
    1. [GetSingerUser](#5-getsingeruser)
* [Products](#products)
    1. [GetAllProducts](#1-getallproducts)
    1. [Create Product](#2-create-product)
    1. [Get Single product](#3-get-single-product)
    1. [Update Product](#4-update-product)
    1. [Delete Product](#5-delete-product)
    1. [UploadImage](#6-uploadimage)
* [Review](#review)
    1. [Get All Reviews](#1-get-all-reviews)
    1. [Create Review](#2-create-review)
    1. [Update Review](#3-update-review)
    1. [Delete Review](#4-delete-review)
* [Order](#order)
    1. [Get All Orders](#1-get-all-orders)
    1. [Create Order](#2-create-order)
    1. [Update Order](#3-update-order)
    1. [Get All My Orders](#4-get-all-my-orders)

--------



## Auth



### 1. RegisterUser



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: http://localhost:5000/auth/register
```



***Body:***

```js        
{
    "name":"Kim",
    "email":"kim@gmail.com",
    "password":"secret"
}
```



### 2. LoginUser



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: http://localhost:5000/auth/login
```



***Body:***

```js        
{
   "email":"ayesiga@gmail.com",
    "password":"secrett"
}
```



### 3. LogoutUser



***Endpoint:***

```bash
Method: GET
Type: RAW
URL: http://localhost:5000/auth/logout
```



***Body:***

```js        
{
    "email":"ayesiga@gmail.com",
    "password":"secrett"
}
```



## User



### 1. GetAllUsers



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://localhost:5000/users
```



### 2. ShowCurrentUser



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://localhost:5000/users/showMe
```



### 3. UpdateUser



***Endpoint:***

```bash
Method: PATCH
Type: RAW
URL: http://localhost:5000/users/updateUser
```



***Body:***

```js        
{
    "name":"Trikcode",
    "email":"together@gmail.com",
    "password":"secrettt"
}
```



### 4. UpdateUserPassword



***Endpoint:***

```bash
Method: PATCH
Type: RAW
URL: http://localhost:5000/users/updateUserPassword
```



***Body:***

```js        
{
    "email":"together@gmail.com",
    "password":"secretttt"
}
```



### 5. GetSingerUser



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://localhost:5000/users/62af85d10e91f8ff3f1d16a4
```



## Products



### 1. GetAllProducts



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://localhost:5000/products
```



### 2. Create Product



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: http://localhost:5000/products
```



***Body:***

```js        
{
    "name":"testproduct",
    "description":"this is anew prodt",
    "category":"office",
    "company":"ikea"
}
```



### 3. Get Single product



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://localhost:5000/products/62b584178f8ae564c2d3bc70
```



### 4. Update Product



***Endpoint:***

```bash
Method: PATCH
Type: 
URL: http://localhost:5000/products/62b584178f8ae564c2d3bc70
```



### 5. Delete Product



***Endpoint:***

```bash
Method: DELETE
Type: 
URL: http://localhost:5000/products/62b584178f8ae564c2d3bc70
```



### 6. UploadImage



***Endpoint:***

```bash
Method: POST
Type: FORMDATA
URL: http://localhost:5000/products/uploadImage
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| image | file |  |



***Body:***

| Key | Value | Description |
| --- | ------|-------------|
| image |  |  |



## Review



### 1. Get All Reviews



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://localhost:5000/reviews
```



### 2. Create Review



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: http://localhost:5000/reviews
```



***Body:***

```js        
{
    "rating":2,
    "title":"Bad product",
    "comment":"too bad",
    "product":"62b585358f8ae564c2d3bc7a"
}
```



### 3. Update Review



***Endpoint:***

```bash
Method: PATCH
Type: RAW
URL: http://localhost:5000/reviews/62b585468f8ae564c2d3bc7e
```



***Body:***

```js        
{
    "rating":1,
    "title":"God product",
    "comment":"too badggd"
  
}
```



### 4. Delete Review



***Endpoint:***

```bash
Method: DELETE
Type: 
URL: http://localhost:5000/reviews/62b585468f8ae564c2d3bc7e
```



## Order



### 1. Get All Orders



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://localhost:5000/orders
```



### 2. Create Order



***Endpoint:***

```bash
Method: POST
Type: RAW
URL: http://localhost:5000/orders
```



***Body:***

```js        
 {
    "tax": 499,
    "shippingFee": 799,
    "items": [
      {
        "name": "bed",
        "price": 2699,
        "image": "https://dl.airtable.com/.attachmentThumbnails/e8bc3791196535af65f40e36993b9e1f/438bd160",
        "amount": 3,
        "product": "62b586a48f8ae564c2d3bc8f"
      },
      {
        "name": "chair",
        "price": 2999,
        "image": "https://dl.airtable.com/.attachmentThumbnails/e8bc3791196535af65f40e36993b9e1f/438bd160",
        "amount": 2,
        "product": "62b586a48f8ae564c2d3bc8f"
      }
    ]
  }
```



### 3. Update Order



***Endpoint:***

```bash
Method: PATCH
Type: RAW
URL: http://localhost:5000/orders/62b0cbb7ceba70da332dbf61
```



***Body:***

```js        
 {
    "tax": 20,
    "shippingFee": 799,
    "items": [
      {
        "name": "bed",
        "price": 2699,
        "image": "https://dl.airtable.com/.attachmentThumbnails/e8bc3791196535af65f40e36993b9e1f/438bd160",
        "amount": 3,
        "product": "62b587258f8ae564c2d3bc9e"
      },
      {
        "name": "chair",
        "price": 2999,
        "image": "https://dl.airtable.com/.attachmentThumbnails/e8bc3791196535af65f40e36993b9e1f/438bd160",
        "amount": 2,
        "product": "62b587258f8ae564c2d3bc9e"
      }
    ]
  }
```



### 4. Get All My Orders



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://localhost:5000/orders/showAllMyOrders
```



---
[Back to top](#e-commerce-api)

>Generated at 2022-06-24 12:59:53 by [docgen](https://github.com/thedevsaddam/docgen)
