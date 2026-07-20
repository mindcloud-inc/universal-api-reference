# Create Token with Refrens

## Endpoint

- **Method:** `POST`
- **Path:** `/authentication`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [Create Token](https://www.refrens.com/api/docs/authentication/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Refrens App ID from the API credentials screen. |
| `appSecret` | body | `string` | yes | Refrens API Secret paired with the App ID. Use this only to generate an access token. |
