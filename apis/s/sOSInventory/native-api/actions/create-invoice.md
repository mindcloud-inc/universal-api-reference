# Create Invoice with SOS Inventory

Creates an invoice in SOS Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/invoice`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [Create Invoice](https://developer.sosinventory.com/apidoc/Invoice)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | body | `string` | no | Invoice number. Use `auto` for SOS automatic numbering. |
| `date` | body | `string` | yes | Transaction date in YYYY-MM-DDTHH:MM:SS format. |
| `customer.name` | body | `string` | yes | Customer name. |
| `comment` | body | `string` | no | Internal company comment. |
| `lines[].item.name` | body | `string` | yes | Item name for the first invoice line. |
| `lines[].quantity` | body | `number` | yes | Quantity for the first invoice line. |
| `lines[].unitPrice` | body | `number` | yes | Per-unit sale price for the first line. |
| `lines[].amount` | body | `number` | yes | Line amount. Must equal quantity multiplied by unit price. |
