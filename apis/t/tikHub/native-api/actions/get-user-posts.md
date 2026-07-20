# Get User Posts with TikHub

Retrieves TikTok posts for a user from TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/web/fetch_user_post`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get User Posts](https://api.tikhub.io/#/TikTok-Web-API/fetch_user_post_api_v1_tiktok_web_fetch_user_post_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `secUid` | query | `string` | yes | User secUid |
| `cursor` | query | `number` | no | Page cursor |
| `count` | query | `number` | no | Number per page |
| `coverFormat` | query | `number` | no | Cover format |
| `post_item_list_request_type` | query | `number` | no | Sort type |
