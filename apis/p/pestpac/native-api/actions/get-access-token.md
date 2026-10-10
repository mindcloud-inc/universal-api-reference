# Get Access Token with PestPac

## Endpoint

- **Method:** `POST`
- **Path:** `https://is.workwave.com/oauth2/token`
- **Base URL:** `https://api.workwave.com/pestpac/v1/`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `scope` | query | `string` | no |
| `grant_type` | body | `string` | no |
| `username` | body | `string` | no |
| `password` | body | `string` | no |
