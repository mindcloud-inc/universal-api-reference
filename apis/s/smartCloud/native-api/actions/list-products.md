# List products with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List products](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id[]` | query | `array<number>` | no | IDs of entities |
| `title` | query | `string` | no | Title name of product |
| `search` | query | `string` | no | Search for entity |
| `is_archived` | query | `boolean` | no | Is this entity archived |
| `is_approved` | query | `boolean` | no | Is this product approved |
| `is_show_market` | query | `boolean` | no | Is this product shown in market |
| `status[]` | query | `array<string>` | no | Product status |
| `sort` | query | `string` | no | Sort key |
| `type` | query | `string` | no | Type of product |
| `abbreviation` | query | `number` | no | Abbreviation of product |
| `order` | query | `string` | no | Sort order |
| `updated_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `updated_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
