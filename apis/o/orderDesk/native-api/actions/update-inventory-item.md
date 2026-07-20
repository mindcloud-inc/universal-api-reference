# Update Inventory Item with Order Desk

Updates an existing inventory item in Order Desk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inventory-items/:inventoryItemId`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Update Inventory Item](https://apidocs.orderdesk.com/?shell=#update-a-single-inventory-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventoryItemId` | path | `string` | yes | Order Desk internal inventory item ID. |
| `name` | body | `string` | yes | Display name of the inventory item. |
| `code` | body | `string` | yes | Unique SKU code for the inventory item. |
| `price` | body | `number` | no | Item price. |
| `stock` | body | `number` | no | Available stock quantity. |
