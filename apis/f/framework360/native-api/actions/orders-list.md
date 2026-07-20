# List Order with Framework360

## Endpoint

- **Method:** `GET`
- **Path:** `orders/list`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [List Order](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `seller` | query | `string` | no | Seller identifier. |
| `id` | query | `number` | no | Specific order ID to filter by. |
| `customer` | query | `number` | no | Customer ID to filter orders by. |
| `page` | query | `number` | no | Results page number. |
| `daterange` | query | `string` | no | Date range filter. |
| `order` | query | `string` | no | Sort order direction. |
| `limit` | query | `number` | no | Maximum number of items per page. |
| `amount` | query | `number` | no | Order amount filter. |
| `query` | query | `string` | no | Free-text search term. |
| `statuses[]` | query | `array<string>` | no | Order statuses to filter by. |
