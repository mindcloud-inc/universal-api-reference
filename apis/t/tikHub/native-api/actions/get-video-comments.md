# Get Video Comments with TikHub

Retrieves comments for a TikTok video from TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/app/v3/fetch_video_comments`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get Video Comments](https://api.tikhub.io/#/TikTok-App-V3-API/fetch_video_comments_api_v1_tiktok_app_v3_fetch_video_comments_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aweme_id` | query | `string` | yes | Video id |
| `cursor` | query | `number` | no | Cursor |
| `count` | query | `number` | no | Number |
