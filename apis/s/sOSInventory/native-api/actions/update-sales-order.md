# Update Sales Order with SOS Inventory

Updates an existing sales order in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/salesorder/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Sales Order](https://developer.sosinventory.com/apidoc/SalesOrder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier for this record. |
| `syncToken` | body | `string` | yes | Current version token for this record. |
| `id` | body | `number` | yes | The sales order id echoed in the request body. |
| `number` | body | `string` | yes | Order number for this sales order. |
| `date` | body | `string` | yes | Transaction date. |
| `customer.id` | body | `number` | yes | Customer for this transaction. |
| `location.id` | body | `number` | yes | Location for this transaction. |
| `customerMessage` | body | `string` | no | Customer message field. |
| `comment` | body | `string` | no | Internal comment for this transaction. |
| `lines[].item.id` | body | `number` | yes | The item this line represents. |
| `lines[].quantity` | body | `number` | yes | The quantity for this line item. |
| `lines[].unitPrice` | body | `number` | yes | The unit price for this item. |
| `lines[].amount` | body | `number` | yes | The amount for this line item. |
