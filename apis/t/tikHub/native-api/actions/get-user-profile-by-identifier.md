# Get User Profile by Identifier with TikHub

Retrieves a TikTok user profile from TikHub by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tiktok/app/v3/handler_user_profile`
- **Base URL:** `https://api.tikhub.io`
- **Official documentation:** [Get User Profile by Identifier](https://api.tikhub.io/#/TikTok-App-V3-API/handler_user_profile_api_v1_tiktok_app_v3_handler_user_profile_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `string` | no | User uid (optional, pure number) |
| `sec_user_id` | query | `string` | no | User sec_user_id |
| `unique_id` | query | `string` | no | User unique_id (username) |
