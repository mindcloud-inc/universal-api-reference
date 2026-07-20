# Refresh Session Token Pair with Airzone Cloud

Creates a refreshed session token pair in Airzone Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/auth/refreshToken/{refreshToken}`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [Refresh Session Token Pair](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refreshToken` | path | `string` | yes | Valid Airzone Cloud refresh token used to issue a new token pair. |
