# Create Invoice with Zoho Books

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Create Invoice](https://www.zoho.com/books/api/v3/invoices/#create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `send` | query | `boolean` | no | Send the invoice to the associated contact persons after creation. |
| `ignore_auto_number_generation` | query | `boolean` | no | Require a custom invoice number instead of auto-generation. |
| `is_quick_create` | query | `boolean` | no | Enable quick create mode for simplified invoice creation. |
| `customer_id` | body | `string` | yes | Unique identifier of the customer for whom the invoice is created. |
| `invoice_number` | body | `string` | no | Custom invoice number when auto-number generation is disabled. |
| `date` | body | `date` | no | Invoice date in yyyy-mm-dd format. |
| `due_date` | body | `date` | no | Invoice due date in yyyy-mm-dd format. |
| `reference_number` | body | `string` | no | External reference number for the invoice. |
| `notes` | body | `string` | no | Notes printed on the invoice. |
| `terms` | body | `string` | no | Terms and conditions for the invoice. |
| `line_items[]` | body | `array<object>` | yes | Line items to include on the invoice. |
| `line_items[].item_id` | body | `string` | yes | Unique identifier of the item to bill. |
| `line_items[].name` | body | `string` | no | Display name for the line item. |
| `line_items[].description` | body | `string` | no | Description for the line item. |
| `line_items[].rate` | body | `number` | no | Unit rate for the line item. |
| `line_items[].quantity` | body | `number` | no | Quantity for the line item. |
