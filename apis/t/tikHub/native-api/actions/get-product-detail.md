# Get Product Detail with TikHub

Retrieves TikTok Shop product details from TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/shop/web/fetch_product_detail`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get Product Detail](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_product_detail_api_v1_tiktok_shop_web_fetch_product_detail_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | query | `string` | yes | Product ID |
| `seller_id` | query | `string` | no | Seller ID (optional) |
| `region` | query | `string` | no | Region code |
