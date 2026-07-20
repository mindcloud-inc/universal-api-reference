# Update Ordered Item Details with Stockpilot

Updates an ordered item in Stockpilot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/orders/ordered-items/:item_id/update`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Update Ordered Item Details](https://api.stockpilot.dev/redoc#operation/update_ordered_item_orders_ordered_items__item_id__update_patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `item_id` | path | `number` | yes |
| `quantity` | body | `number` | yes |
