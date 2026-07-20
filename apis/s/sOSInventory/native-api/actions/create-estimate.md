# Create Estimate with SOS Inventory

Creates an estimate in SOS Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/estimate`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Create Estimate](https://developer.sosinventory.com/apidoc/Estimate)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | yes | Order number for this estimate. Use auto for automatic numbering. |
| `date` | body | `string` | yes | Transaction date. |
| `customer.id` | body | `number` | yes | Customer for this transaction. |
| `customerMessage` | body | `string` | no | Customer message field. |
| `comment` | body | `string` | no | Internal comment for this transaction. |
| `lines[].item.id` | body | `number` | yes | The item this line represents. |
| `lines[].quantity` | body | `number` | yes | The quantity of this item for this line. |
| `lines[].unitprice` | body | `number` | yes | The unit price for this item. |
| `lines[].amount` | body | `number` | yes | The sales amount for this line item. |
