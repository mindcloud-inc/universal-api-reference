# List Plans with PayWhirl

Retrieves subscription plans from PayWhirl.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [List Plans](https://api.paywhirl.com/#plans)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after_id` | query | `number` | no | Return plans with IDs greater than this value. |
| `before_id` | query | `number` | no | Return plans with IDs lower than this value. |
| `limit` | query | `number` | no | Number of plan records to return. |
| `order_direction` | query | `string` | no | Sort direction. Use asc or desc. |
| `order_key` | query | `string` | no | Plan field to sort by. |
