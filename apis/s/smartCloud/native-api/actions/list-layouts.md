# List layouts with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/layouts`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List layouts](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id[]` | query | `array<number>` | no | IDs of entities |
| `title` | query | `string` | no | Title name of layout |
| `store_id` | query | `string` | no | ID of layout same accross all versions |
| `is_enabled` | query | `boolean` | no | Is this version enabled |
| `product_id` | query | `number` | no | ID of product |
| `sort` | query | `string` | no | Sort key |
| `search` | query | `string` | no | Search for entity |
| `is_archived` | query | `boolean` | no | Is this entity archived |
| `order` | query | `string` | no | Sort order |
| `updated_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `updated_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
