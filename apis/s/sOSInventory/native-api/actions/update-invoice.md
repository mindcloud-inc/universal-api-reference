# Update Invoice with SOS Inventory

Updates an existing invoice in SOS Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/invoice/:id`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Update Invoice](https://developer.sosinventory.com/apidoc/Invoice)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Invoice ID in the request path. |
| `number` | body | `string` | yes | Current invoice number. |
| `date` | body | `string` | yes | Transaction date in YYYY-MM-DDTHH:MM:SS format. |
| `customer.name` | body | `string` | yes | Customer name. |
| `comment` | body | `string` | no | Internal company comment. |
| `lines[].item.name` | body | `string` | yes | Item name for the first invoice line. |
| `lines[].quantity` | body | `number` | yes | Quantity for the first invoice line. |
| `lines[].unitPrice` | body | `number` | yes | Per-unit sale price for the first line. |
| `lines[].amount` | body | `number` | yes | Line amount. Must equal quantity multiplied by unit price. |
