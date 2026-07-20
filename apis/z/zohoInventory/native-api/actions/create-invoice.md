# Create Invoice with Zoho Inventory

Creates a new invoice in Zoho Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Create Invoice](https://www.zoho.com/inventory/api/v1/invoices/#create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
| `customer_id` | body | `string` | yes | Customer to bill on the invoice. |
| `invoice_number` | body | `string` | no | Invoice number when auto numbering is disabled. |
| `send` | query | `boolean` | no | Whether to send the invoice after creation. |
| `ignore_auto_number_generation` | query | `boolean` | no | — |
| `date` | body | `string` | no | Invoice date in YYYY-MM-DD format. |
| `due_date` | body | `string` | no | Invoice due date in YYYY-MM-DD format. |
| `reference_number` | body | `string` | no | External reference number for the invoice. |
| `line_items[]` | body | `array<object>` | yes | One or more invoice line items. |
| `line_items[].item_id` | body | `string` | yes | Item to add on this invoice line. |
| `line_items[].quantity` | body | `number` | yes | Quantity to invoice for this line. |
| `line_items[].rate` | body | `number` | no | Rate for this invoice line item. |
