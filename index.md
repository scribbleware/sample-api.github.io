# Sample API Documentation

This repository explains how to use a sample YAML-based OAuth 2 Open API that allows access to a catalog and authenticated access to users, orders, shopping carts, payments and shipments information.

## Contents

- [Overview]()
- [Authentication]()
- Endpoints
  - [Carts]()
  - [Catalogs]()
  - [Customers]()
  - [Orders]()
  - [Payments]()
  - [Shipments]()



## Overview


This sample API allows access to a catalog and authenticated access to users, orders, shopping carts, payments and shipments information at the following endpoints:

| Service/Endpoint | YAML File      | User Specific? |
| ---------------- | -------------- | -------------- |
| carts            | carts.yaml     | yes            |
| catalogs         | catalogs.yaml  | no             |
| customers        | users.yaml     | yes            | 
| orders           | orders.yaml    | yes            |
| payments         | payments.yaml  | yes            |
| shipments        | shipments.yaml | yes            |


## Authorization

You will need an access token to access the sample API endpoints. An OAuth token that contains the customerID grants API access.

Authorization (customer ID): 043fa14b-f6b5-4b96-9cd3-b5f0819b6283


## Carts

Get or update cart items for a specific customer


### Get Cart Items 

This endpoint retrieves all cart items for a specific customer.


#### HTTP Request 

GET https://example.com/api/v1/c/cart/<ID>/items

  
#### Query Parameters

| Parameter | Description                |
| --------- | -------------------------- |  
| ID        | The customer ID            |  

  
### Update a Cart

This endpoint updates a cart for a specific customer.

#### HTTP Request 

PUT https://example.com/api/v1/c/carts/<ID>/items

#### Query Parameters

| Parameter | Description                |
| --------- | -------------------------- |  
| ID        | The customer ID            |  
 


## Catalogs

All users (authenticated or unauthenticated) can view available catalog items.

### Get All Catalog Items 

This endpoint retrieves all catalog items.

#### HTTP Request 

GET https://example.com/api/v1/c/catalogs

#### Query Parameters

None


### Add a Catalog Item

This endpoint adds a catalog items.

#### HTTP Request 

POST https://example.com/api/v1/c/catalogs

#### Query Parameters

None



### Update a Catalog Item

This endpoint updates a catalog item.

#### HTTP Request 

PATCH https://example.com/api/v1/c/catalogs/<ID>

#### Query Parameters

| Parameter | Description                |
| --------- | -------------------------- |  
| ID        | The ID of the catalog item |  


### Delete a Catalog Item

This endpoint deletes a catalog item.

#### HTTP Request 

DELETE https://example.com/api/v1/c/catalogs/<ID>

#### Query Parameters

| Parameter | Description                |
| --------- | -------------------------- |  
| ID        | The ID of the catalog item | 


## Customers

Retrieve and maintain customer data using this endpoint.

### Get A Specific Customer 

This endpoint retrieves a single customer.

#### HTTP Request 

GET https://example.com/api/v1/c/customers/<ID>

#### Query Parameters

| Parameter | Description                |
| --------- | -------------------------- |  
| ID        | The ID of the catalog item |  



### Add a Specific Customer

This endpoint adds a specific customer.

#### HTTP Request 

POST https://example.com/api/v1/c/customers

#### Query Parameters

None



### Update a Specific Customer

This endpoint updates a specific customer.

#### HTTP Request 

PATCH https://example.com/api/v1/c/customers/<ID>

#### Query Parameters

| Parameter | Description                |
| --------- | -------------------------- |  
| ID        | The ID of the customer |  


### Delete a Specific Customer

This endpoint deletes a specific customer.

#### HTTP Request 

DELETE https://example.com/api/v1/c/customers/<ID>

#### Query Parameters

| Parameter | Description                |
| --------- | -------------------------- |  
| ID        | The ID of the customer | 


## Orders

List all orders for a customer or add to a specific customer order using this endpoint.

### Get All Orders for A Specific Customer 

This endpoint retrieves all orders for a single customer.

#### HTTP Request 

GET https://example.com/api/v1/c/orders/<ID>

#### Query Parameters

| Parameter | Description                |
| --------- | -------------------------- |  
| ID        | The ID of the customer     |  

Note: The order endpoint gets the shipment status from the shipments endpoint, using the shipmentID from successful shipments. [See Shipments]() for more information about the shipmentID.

  
  
  
## Errors

This example API sends a variety of status codes but can be generally categorized as below.

| Error Code | Meaning       |
| ---------- | ------------- |
| 2XX        | Success       |
| 4XX        | Client errors<br> e.g. request validation errors | 
| 5xx        | Server errors<br> e.g. database connectivity or internal service call errors | 
  

  
  
  
You can use the [editor on GitHub](https://github.com/scribbleware/sample-api.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/scribbleware/sample-api.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
