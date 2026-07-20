# Update Estimate with SOS Inventory

Updates an existing estimate in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/estimate/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Estimate](https://developer.sosinventory.com/apidoc/Estimate)

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
| `id` | body | `number` | yes | The estimate id echoed in the request body. |
| `number` | body | `string` | yes | Order number for this estimate. |
| `date` | body | `string` | yes | Transaction date. |
| `customer.id` | body | `number` | yes | Customer for this transaction. |
| `customerMessage` | body | `string` | no | Customer message field. |
| `comment` | body | `string` | no | Internal comment for this transaction. |
| `lines[].item.id` | body | `number` | yes | The item this line represents. |
| `lines[].quantity` | body | `number` | yes | The quantity of this item for this line. |
| `lines[].unitprice` | body | `number` | yes | The unit price for this item. |
| `lines[].amount` | body | `number` | yes | The sales amount for this line item. |
