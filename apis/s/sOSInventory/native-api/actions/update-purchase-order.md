# Update Purchase Order with SOS Inventory

Updates an existing purchase order in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/purchaseorder/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Purchase Order](https://developer.sosinventory.com/apidoc/PurchaseOrder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Purchase order ID in the request path. |
| `syncToken` | body | `number` | no | Current record version from the latest GET response. |
| `number` | body | `string` | yes | Current purchase order number. |
| `date` | body | `string` | yes | Transaction date in YYYY-MM-DDTHH:MM:SS format. |
| `vendor.name` | body | `string` | yes | Vendor name. |
| `location.name` | body | `string` | yes | Location name. |
| `comment` | body | `string` | no | Internal company comment. |
| `lines[].item.name` | body | `string` | yes | Item name for the first purchase-order line. |
| `lines[].quantity` | body | `number` | yes | Quantity for the first purchase-order line. |
| `lines[].unitPrice` | body | `number` | yes | Per-unit purchase cost for the first line. |
| `lines[].amount` | body | `number` | yes | Line amount. Must equal quantity multiplied by unit price. |
