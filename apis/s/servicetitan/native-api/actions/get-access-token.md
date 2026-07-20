# Get Access Token with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `https://{authUrl}/connect/token`
- **Base URL:** `https://{baseUrl}/`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `grant_type` | body | `string` | no |
| `tenant` | body | `string` | no |
| `client_id` | body | `string` | no |
| `client_secret` | body | `string` | no |
