# Update Invoice with Invoice Ninja

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Update Invoice](https://api-docs.invoicing.co/#tag/invoices/operation/updateInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `due_date` | body | `string` | no | The due date in YYYY-MM-DD format. |
| `id` | path | `string` | yes | The invoice hashed id. |
| `private_notes` | body | `string` | no | Private notes for the invoice. |
