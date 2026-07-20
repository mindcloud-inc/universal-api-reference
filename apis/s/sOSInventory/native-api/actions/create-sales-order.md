# Create Sales Order with SOS Inventory

Creates a sales order in SOS Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/salesorder`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Create Sales Order](https://developer.sosinventory.com/apidoc/SalesOrder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | Order number for this sales order. Use auto for automatic numbering. |
| `date` | body | `string` | yes | Transaction date. |
| `customer.id` | body | `number` | yes | Customer for this transaction. |
| `location.id` | body | `number` | yes | Location for this transaction. |
| `customerMessage` | body | `string` | no | Customer message field. |
| `comment` | body | `string` | no | Internal comment for this transaction. |
| `lines[].item.id` | body | `number` | yes | The item this line represents. |
| `lines[].quantity` | body | `number` | yes | The quantity for this line item. |
| `lines[].unitPrice` | body | `number` | yes | The unit price for this item. |
| `lines[].amount` | body | `number` | yes | The amount for this line item. |
