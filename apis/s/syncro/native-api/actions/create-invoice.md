# Create Invoice with Syncro

Creates a new invoice in Syncro.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Create Invoice](https://api-docs.syncromsp.com/#/Invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `number` | yes | Required customer record ID for the new invoice. |
| `number` | body | `string` | yes | Required invoice number string. |
| `date` | body | `date` | yes | Required invoice date. |
| `due_date` | body | `date` | no | — |
| `ticket_id` | body | `number` | no | — |
| `location_id` | body | `number` | no | — |
| `contact_id` | body | `number` | no | — |
| `po_number` | body | `string` | no | — |
| `note` | body | `string` | no | — |
| `line_items[]` | body | `array<object>` | no | Array of invoice line item objects. |
| `line_items[].item` | body | `string` | no | — |
| `line_items[].name` | body | `string` | no | — |
| `line_items[].product_id` | body | `number` | no | — |
| `line_items[].quantity` | body | `number` | no | — |
| `line_items[].cost` | body | `number` | no | — |
| `line_items[].price` | body | `number` | no | — |
| `line_items[].discount_percent` | body | `number` | no | — |
| `line_items[].taxable` | body | `boolean` | no | — |
| `line_items[].upc_code` | body | `string` | no | — |
| `line_items[].tax_note` | body | `string` | no | — |
| `line_items[].wholesale` | body | `number` | no | — |
| `line_items[].invoice_bundle_id` | body | `number` | no | — |
| `line_items[].tax_rate_id` | body | `number` | no | — |
| `line_items[].user_id` | body | `number` | no | — |
| `line_items[].position` | body | `number` | no | — |
| `id` | body | `number` | no | Explicit invoice ID field documented in Syncro's create payload schema. |
| `balance_due` | body | `number` | no | — |
| `customer_business_then_name` | body | `string` | no | — |
| `created_at` | body | `date` | no | — |
| `updated_at` | body | `date` | no | — |
| `subtotal` | body | `string` | no | — |
| `total` | body | `string` | no | — |
| `tax` | body | `string` | no | — |
| `verified_paid` | body | `boolean` | no | — |
| `tech_marked_paid` | body | `boolean` | no | — |
| `pdf_url` | body | `string` | no | — |
| `is_paid` | body | `boolean` | no | — |
| `hardwarecost` | body | `number` | no | — |
