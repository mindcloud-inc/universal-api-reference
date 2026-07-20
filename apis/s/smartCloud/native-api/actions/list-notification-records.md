# List notification record with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/notification-records`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List notification record](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isRead` | query | `boolean` | no | Is this notification read |
| `sort` | query | `string` | no | Sort key |
| `search` | query | `string` | no | Search for entity |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
| `created_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
