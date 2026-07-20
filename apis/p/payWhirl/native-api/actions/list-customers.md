# List Customers with PayWhirl

Retrieves customers from PayWhirl.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [List Customers](https://api.paywhirl.com/#customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after_id` | query | `number` | no | Return customers with IDs greater than this value. |
| `before_id` | query | `number` | no | Return customers with IDs lower than this value. |
| `keyword` | query | `string` | no | Optional keyword filter. |
| `limit` | query | `number` | no | Number of customer records to return. |
| `order_direction` | query | `string` | no | Sort direction. Use asc or desc. |
| `order_key` | query | `string` | no | Customer field to sort by. |
