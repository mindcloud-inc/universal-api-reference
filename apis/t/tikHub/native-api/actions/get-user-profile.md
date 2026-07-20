# Get User Profile with TikHub

Retrieves a TikTok user profile from TikHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/web/fetch_user_profile`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get User Profile](https://api.tikhub.io/#/TikTok-Web-API/fetch_user_profile_api_v1_tiktok_web_fetch_user_profile_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uniqueId` | query | `string` | no | User uniqueId |
| `secUid` | query | `string` | no | User secUid |
