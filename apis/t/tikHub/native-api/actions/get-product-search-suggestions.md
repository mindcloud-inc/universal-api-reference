# Get Product Search Suggestions with TikHub

Finds TikTok Shop product search suggestions in TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/shop/web/fetch_search_word_suggestion`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get Product Search Suggestions](https://api.tikhub.io/#/TikTok-Shop-Web-API/fetch_search_word_suggestion_api_v1_tiktok_shop_web_fetch_search_word_suggestion_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_word` | query | `string` | yes | Search keyword |
| `lang` | query | `string` | no | Language |
| `region` | query | `string` | no | Region code |
