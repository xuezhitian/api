# User API
## 1. Product
### 1.1 List Product

> GET /api/user/v1/products

Response:
```

{
    "code": 0,
    "message": "success",
    "data": [
        {
             "product_id": 1,
             "name": "phone",
             "description" : "miaoshu",
             "price" : 1000,
             "img" : "http://www.dsad.com"
        }
    ]
}

```

### 1.2 Product Details

> GET /api/user/v1/product/[productId]

Response:
```
{
    "code" : 0,
    "message" : "success",
    "data": [
        {
            "product_id" : 1,
            "name" : "MeiZu mobile",
            "description" : "this is the product",
            "price" : 2000,
            "img" : "https://item.jd.com/1238332.html"
            "sku" : [
                {
                    "sku_id" : 1,
                    "name" : "MagBlue",
                    "description" : "blue phone",
                    "img" : "http://www.cads.com",
                    "price" : 1000 
                },
                {
                    "sku_id" : 2,
                    "name" : "MagBlack",
                    "description" : "red phone",
                    "img" : "http://wta.sad.cn",
                    "price" : 1000  
                 }
              ]
         } 
    ]
}
```

## 2. Cart

### 2.1 Add Cart

> POST /api/user/v1/cart

Request:
```
{
    "code" : 0,
    "message" : "success",
    "data" : [
        {
            "user_id" : 1,
            "cart_id" : 1,
            "sku_id" : 1,
            "product_id" : 1,
            "select_item_count" : 13,
            "total_price" : 550,
            "real_total_price" : 124,
            "order_count" : 13
        }
    ]
}

```

### 2.2 List Cart

> GET /api/user/v1/cart/

Response:
```
{
    "code" : 0,
    "message" : "success",
    "data" : [
        {
            "cart_id" : 1,
            "user_id" ; 1,
            "product_id" : 1,
            "sku_id" : 1,
            "selected_item_count" : 12,
            "order_count" : 12
        }    
    ]
}

```

#### 2.3 Delete Cart

> DELETE /api/user/v1/cart/[cartId]

```
{
        "code" : 0,
        "message" : "success"
}
         

```


## 3 Order
### 3.1 List Order

> GET /api/user/v1/order

Response:
```
{
    "code" : 0,
    "message" : "success",
    "data" : [
        {
            "order_id" : 1,
            "user_id" : 1,
            "product_id" : 1,
            "order_no" : 15664646,
            "payment": 1044,
            "postage" : 5,
            "status" : 10,
            "payment_time" : "2015-10-24",
            "send_time" : "2015-10-26",
            "end_time" : "2015-11-01",
            "close_time" : "2015-11-05"
        }
    ]
}

```



### 3.2 Cancel Order

> DELETE /api/user/v1/order/[order]

Response: 
```  
{
     "code" : 0,
     "message" : "success"    
    
}


```


