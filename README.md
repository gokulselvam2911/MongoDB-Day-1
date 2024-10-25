
# MongoDB Query Operations

## Queries

### 1. Find all the information about each product
```javascript
db.products.find({})
```
  ![1 Find all the information about each product](1-Find-all-the-information-about-each-product.png)

### 2. Find the product prices that are between 400 and 800
```javascript
db.products.find({ product_price: { $gte: 400, $lte: 800 } })
```
 ![2 Find the product prices that are between 400 and 800](2-Find-the-product-prices-that-are-between-400-and-800.png)

### 3. Find the product prices that are not between 400 and 600
```javascript
db.products.find({ product_price: { $not: { $gte: 400, $lte: 600 } } })
```
 ![3 Find the product prices that are not between 400 and 600](3-Find-the-product-prices-that-are-not-between-400-and-600.png)

### 4. List the four products that have a price greater than 500
```javascript
db.products.find({ product_price: { $gt: 500 } }).limit(4)
```
 ![List the four products that have a price greater than 500](4-List-the-four-products-that-have-a-price-greater-than-500.png)

### 5. Find the product name and product material of each product
```javascript
db.products.find({}, { product_name: 1, product_material: 1, _id: 0 })
```
 ![Find the product name and product material of each product](5-Find-the-product-name-and-product-material-of-each-product.png)

### 6. Find the product with a row id of 10
```javascript
db.products.find({ id: "10" })
```
 ![Find the product with a row id of 10](6-Find-the-product-with-a-row-id-of-10.png)

### 7. Find only the product name and product material
```javascript
db.products.find({}, { product_name: 1, product_material: 1, _id: 0 })
```
 ![Find only the product name and product material](7-Find-only-the-product-name-and-product-material.png)

### 8. Find all products that contain "Soft" in product material
```javascript
db.products.find({ product_material: "Soft" })
```
 ![Find all products that contain 'Soft' in product material](8-Find-all-products-that-contain-Soft-in-product-material.png)

### 9. Find products that have product color "indigo" and product price 492.00
```javascript
db.products.find({ product_color: "indigo", product_price: 492.00 })
```
 ![Find products that have product color 'indigo' and product price 492.00](9-Find-products-that-have-product-color-indigo-and-product-price-492.png)

### 10. Delete products with a product price value of 28
```javascript
db.products.deleteMany({ product_price: 28 })
```
 ![Delete products with a product price value of 28](10-Delete-products-with-a-product-price-value-of-28.png)

