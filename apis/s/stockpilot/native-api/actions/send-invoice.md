# Send Invoice with Stockpilot

Sends an invoice for an order in Stockpilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/send`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Send Invoice](https://api.stockpilot.dev/redoc#operation/send_invoice_invoices_send_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_pk` | body | `number` | yes |
| `invoice` | body | `file` | no |
