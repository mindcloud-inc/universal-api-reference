# Delete Inventory Item with Order Desk

Deletes an existing inventory item from Order Desk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/inventory-items/:inventoryItemId`
- **Base URL:** `https://app.orderdesk.me/api/v2`
- **Official documentation:** [Delete Inventory Item](https://apidocs.orderdesk.com/?shell=#delete-an-inventory-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventoryItemId` | path | `string` | yes | Order Desk internal inventory item ID. |
