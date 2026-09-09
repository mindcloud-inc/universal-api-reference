# Token API - refresh_token with Walmart

## Endpoint

- **Method:** `POST`
- **Path:** `v3/token`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Token API - refresh_token](https://developer.walmart.com/us-marketplace/reference/tokenapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `grant_type` | body | `list<string>` | no |
| `refresh_token` | body | `list` | no |
