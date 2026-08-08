# Get Token with Workday

Exchange a refresh token for a new Workday access token.

## Endpoint

- **Method:** `POST`
- **URL:** `{tokenEndpoint}`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `grant_type` | body | `string` | no |
| `refresh_token` | body | `string` | no |
