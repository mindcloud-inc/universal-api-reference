# List Urls with Prerender.io

Retrieves URLs from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/urls`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Urls](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `adaptiveType` | query | `string` | no |
| `limit` | query | `number` | yes |
| `offset` | query | `number` | yes |
| `wildcard` | query | `string` | yes |
