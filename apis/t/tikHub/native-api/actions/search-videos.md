# Search Videos with TikHub

Finds TikTok videos in TikHub by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/web/fetch_search_video`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Search Videos](https://api.tikhub.io/#/TikTok-Web-API/fetch_search_video_api_v1_tiktok_web_fetch_search_video_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | query | `string` | yes | Search keyword |
| `count` | query | `number` | no | Number per page |
| `offset` | query | `number` | no | Page cursor |
| `search_id` | query | `string` | no | Search id, need to provide when paging |
| `cookie` | query | `string` | no | User cookie(if needed) |
