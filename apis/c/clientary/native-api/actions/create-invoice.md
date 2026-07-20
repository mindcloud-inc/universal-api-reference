# Create Invoice with Clientary

Creates a new invoice in Clientary.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Create Invoice](https://www.clientary.com/api/invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice.client_id` | body | `number` | no | Optionally associate the invoice with a client. |
| `invoice.currency_code` | body | `string` | yes | The ISO currency code for the invoice. |
| `invoice.date` | body | `string` | yes | The invoice issue date (YYYY-MM-DD). |
| `invoice.due_date` | body | `string` | yes | The invoice due date (YYYY-MM-DD). |
