# MongoDB Aggregation Framework Assignment - EASY

## 1. List All Products in the "Electronics" Category:

```
db.products.aggregate([{
$match: {
category: "Electronics"}
}])
```
![alt text](image-1.png)

## 2. Count Products per Category:
```
db.products.aggregate([{
$group: {
_id: "$category",
count: {$sum: 1}
}}])
```
![alt text](image.png)

## 3. Product Names and Prices, Sorted by Price (Descending):
```
db.products.aggregate([
  {$project: {
_id: 0,
name: "$name",
price: "$price"}},
	{$sort: {
price: 1}}
])
```
![alt text](image-2.png)