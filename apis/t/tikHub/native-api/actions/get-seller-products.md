# Get Seller Products with TikHub

Retrieves TikTok Shop products for a seller from TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/shop/web/fetch_seller_products_list`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get Seller Products](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_seller_products_list_api_v1_tiktok_shop_web_fetch_seller_products_list_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `seller_id` | query | `string` | yes | Seller ID |
| `search_params` | query | `string` | no | Search params (for pagination) |
| `region` | query | `string` | no | Region code |
