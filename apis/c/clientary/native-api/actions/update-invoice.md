# Update Invoice with Clientary

Updates an invoice in Clientary by invoice ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Update Invoice](https://www.clientary.com/api/invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Clientary invoice ID. |
| `invoice.currency_code` | body | `string` | no | The ISO currency code for the invoice. |
| `invoice.due_date` | body | `string` | no | The invoice due date (YYYY-MM-DD). |
