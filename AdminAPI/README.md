# Admin API
## 1 User Managemet 
### 1.1 List User

> GET /api/admin/v1/users

Response:
```
{
    "code" : 0,
    "message" : "success",
    "data" : [
        {
           "user_id" : 1,
           "name" : "WangZhiHao",
           "phone" : 1575557555,
           "gender" : 0,
           "password" : 156849
        }   
    ]
}

```

### 1.2 Delete User

> DELETE /api/admin/v1/user/[userId]

Response:
```
{
    "code" : 0,
    "message" : "success"
}

```

## 2 Product
### 2.1 List Product

> GET /api/admin/v1/products

Response:
```
{
    "code" : 0,
    "message" : "success",
    "data" : [
        {
            "product_id" : 1,
            "name" : "phone",
            "description" ; "blue phone",
            "price" : 200
            ]
        }
    ]
}

```

### 2.2 Add Product

> POST /api/admin/v1/product

Request:
```
{
    "code" : 0,
    "message" : "success",
    "data" : [
        {
            "product_id" : 1,
            "name" : "phone',
            "descriptio" : "blue phone",
            "price" : 200,
            "img" : http://www.asd.awd"
        }
    ]    
}

```

### 2.3 Delete Product

> DELETE /api/admin/v1/prouct/[productId]

#### Response:
```
{
    "code" : 0,
    "message" : "success"
}

```

### 2.4 Update Product

> PATCH /api/admin/v1/product/[productId]

Response:
```
{
    "code" : 0,
    "message" : "success",
    "data" : [
        {
            "product_id" : 1,
            "name" : "phone",
            "description": "black",
            "price" : 2000,
            "img" : http://www.asd.cn"
        }
    ]
}

```

## 3 Order
### 3.1 List Order

> GET /api/admin/v1/orders

Response:
```
{
    "code" : 0,
    "message" : "success",
    "data" : [
        {
           "order_id" :1,
           "user_id" : 1,
           "product_id" : 1,
           "order_no" : 5456465,
           "payment" : 135,
           "payment_type" : 10,
           "postage" : 10,
           "status" : 10,
           "payment_time" : "2015-10-24",
           "send_time" : "2015-10-26",
           "end_time" : "2015-11-01",
           "close_time" : "2015-11-05"
        } 
    ]
}

```
