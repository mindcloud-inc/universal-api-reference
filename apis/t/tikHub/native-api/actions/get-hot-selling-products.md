# Get Hot Selling Products with TikHub

Retrieves hot-selling TikTok Shop products from TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/shop/web/fetch_hot_selling_products_list`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get Hot Selling Products](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_hot_selling_products_list_api_v1_tiktok_shop_web_fetch_hot_selling_products_list_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `region` | query | `string` | no | Region code |
| `count` | query | `number` | no | Number of products to return |
