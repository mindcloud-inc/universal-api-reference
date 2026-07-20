# Search Products with TikHub

Finds TikTok Shop products in TikHub by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/shop/web/fetch_search_products_list`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Search Products](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_search_products_list_api_v1_tiktok_shop_web_fetch_search_products_list_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_word` | query | `string` | yes | Search keyword |
| `offset` | query | `number` | no | Offset |
| `page_token` | query | `string` | no | Page token |
| `region` | query | `string` | no | Region code |
