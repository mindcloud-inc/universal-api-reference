# Create Invoice with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Create Invoice](https://api-docs.invoicing.co/#tag/invoices/operation/storeInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | yes | The client hashed id. |
| `date` | body | `string` | no | The invoice date in YYYY-MM-DD format. |
| `due_date` | body | `string` | no | The due date in YYYY-MM-DD format. |
| `line_items` | body | `list<object>` | no | Array of invoice line item objects. |
