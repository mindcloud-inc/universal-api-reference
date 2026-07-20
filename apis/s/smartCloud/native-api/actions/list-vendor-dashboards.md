# List dashboards with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/dashboards`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List dashboards](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id[]` | query | `array<number>` | no | IDs of entities |
| `title` | query | `string` | no | Dashboard title |
| `is_enabled` | query | `boolean` | no | Whether the dashboard is enabled |
| `product_id` | query | `number` | no | Product identifier |
| `sort` | query | `string` | no | Dashboard sort field |
| `search` | query | `string` | no | Search for entity |
| `is_archived` | query | `boolean` | no | Is this entity archived |
| `order` | query | `string` | no | Sort order |
| `updated_from` | query | `date` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `updated_to` | query | `date` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_from` | query | `date` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | query | `date` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
