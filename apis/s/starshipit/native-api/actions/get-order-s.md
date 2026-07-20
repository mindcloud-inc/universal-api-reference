# Get Order(s) with Starshipit

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Get Order(s)](https://api-docs.starshipit.com/#0aef707f-e2f5-493a-a382-8235c00c9c18)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | query | `string` | no | The unique numeric identifier for the order |
| `order_number` | query | `string` | no | The identifier of the order pulled from source e-Commerce platform |
| `status` | query | `string` | no | — |
| `filter` | query | `string` | no | — |
| `include` | query | `string` | no | — |
| `sort_column` | query | `string` | no | Order field to sort by. |
| `sort_direction` | query | `string` | no | — |
| `page_number` | query | `string` | no | — |
