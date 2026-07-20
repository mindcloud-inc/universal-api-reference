# Generate Access Token with Nvoip

## Endpoint

- **Method:** `POST`
- **Path:** `/oauth/token`
- **Base URL:** `https://api.nvoip.com.br/v2`
- **Official documentation:** [Generate Access Token](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/index.js)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grant_type` | body | `string` | yes | OAuth grant type documented by Nvoip for token generation. |
| `password` | body | `string` | yes | Paste the Nvoip User Token here to generate a fresh access token. |
| `username` | body | `string` | yes | Nvoip Numbersip or User SIP used to generate the access token. |
