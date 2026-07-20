# Get User Info with TikTok Accounts

Retrieves profile information for the authenticated user in TikTok.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/user/info/`
- **Base URL:** `https://open.tiktokapis.com`
- **Official documentation:** [Get User Info](https://developers.tiktok.com/doc/tiktok-api-v2-get-user-info/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | yes | Comma-separated TikTok user fields to return. The default includes only fields authorized by user.info.basic. |
