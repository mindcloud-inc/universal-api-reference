# Delete Entire Order with Stockpilot

Deletes an order from Stockpilot.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orders/:order_id`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Delete Entire Order](https://api.stockpilot.dev/redoc#operation/delete_order_orders__order_id__delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | path | `number` | yes |
| `book_back` | body | `boolean` | no |
