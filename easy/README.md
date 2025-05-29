# MongoDB Aggregation Framework Assignment - EASY

```
db.products.aggregate([{
$match: {
category: "Electronics"}
}])
```
![alt text](image-1.png)

2
```
db.products.aggregate([{
$group: {
_id: "$category",
count: {$sum: 1}
}}])
```
![alt text](image.png)

3
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