# List api tokens with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/api-tokens`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List api tokens](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Name name of api token |
| `search` | query | `string` | no | Search for entity |
| `updated_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `updated_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `sort` | query | `string` | no | Sort key |
| `order` | query | `string` | no | Sort order |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
