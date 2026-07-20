# Cancel Order Item with Keysender

Cancels an order item in Keysender.

## Endpoint

- **Method:** `POST`
- **Path:** `/catalog/order/cancel-item`
- **Base URL:** `https://panel.keysender.co.uk/api/v1.0`
- **Official documentation:** [Cancel Order Item](https://panel.keysender.co.uk/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `increment_id` | body | `string` | no |
| `line_item_id` | body | `string` | no |
