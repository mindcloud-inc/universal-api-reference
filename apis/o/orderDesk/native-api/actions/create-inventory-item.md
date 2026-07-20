# Create Inventory Item with Order Desk

Creates a new inventory item in Order Desk.

## Endpoint

- **Method:** `POST`
- **Path:** `/inventory-items`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Create Inventory Item](https://apidocs.orderdesk.com/?shell=#create-an-inventory-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name of the inventory item. |
| `code` | body | `string` | yes | Unique SKU code for the inventory item. |
| `price` | body | `number` | no | Item price. |
| `stock` | body | `number` | no | Available stock quantity. |
