# Update Invoice with Zoho Inventory

Updates an existing invoice in Zoho Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:invoice_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Update Invoice](https://www.zoho.com/inventory/api/v1/invoices/#update-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `string` | yes | The Zoho Inventory invoice_id for the invoice. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
| `customer_id` | body | `string` | yes | Customer to bill on the invoice. |
| `invoice_number` | body | `string` | no | Invoice number for this invoice. |
| `date` | body | `string` | no | Invoice date in YYYY-MM-DD format. |
| `due_date` | body | `string` | no | Invoice due date in YYYY-MM-DD format. |
| `reference_number` | body | `string` | no | External reference number for the invoice. |
| `line_items[]` | body | `array<object>` | yes | One or more invoice line items. |
| `line_items[].line_item_id` | body | `string` | no | Existing line item identifier when updating a line. |
| `line_items[].item_id` | body | `string` | yes | Item to set on this invoice line. |
| `line_items[].quantity` | body | `number` | yes | Quantity to invoice for this line. |
| `line_items[].rate` | body | `number` | no | Rate for this invoice line item. |
