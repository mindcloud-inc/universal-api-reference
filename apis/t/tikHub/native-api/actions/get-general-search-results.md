# Get General Search Results with TikHub

Retrieves general TikTok search results from TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/app/v3/fetch_general_search_result`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get General Search Results](https://api.tikhub.io/#/TikTok-App-V3-API/fetch_general_search_result_api_v1_tiktok_app_v3_fetch_general_search_result_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Keyword |
| `offset` | query | `number` | no | Offset |
| `count` | query | `number` | no | Number |
| `sort_type` | query | `number` | no | Sort type |
| `publish_time` | query | `number` | no | Publish time |
