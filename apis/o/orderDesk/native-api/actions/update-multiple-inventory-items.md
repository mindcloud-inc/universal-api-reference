# Update Multiple Inventory Items with Order Desk

Updates multiple inventory items in Order Desk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/batch-inventory-items`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Update Multiple Inventory Items](https://apidocs.orderdesk.com/?shell=#update-multiple-inventory-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventoryItems[].id` | body | `string` | yes | Order Desk internal inventory item ID. |
| `inventoryItems[].name` | body | `string` | yes | Display name of the inventory item. |
| `inventoryItems[].code` | body | `string` | yes | Unique SKU code for the inventory item. |
| `inventoryItems[].price` | body | `number` | no | Item price. |
| `inventoryItems[].stock` | body | `number` | no | Available stock quantity. |
