# Create Invoice with SWELLEnterprise

Creates a new invoice in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/finance/invoices`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Invoice](https://dashboard.swellsystem.com/docs#finance-invoices-POSTapi-v1-finance-invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_number` | body | `string` | yes | The invoice number. |
| `status` | body | `string` | yes | The invoice status. |
| `contact_id` | body | `number` | no | The contact ID. |
| `invoice_date` | body | `date` | yes | The invoice date. |
| `company_id` | body | `number` | no | The company ID. |
| `due_date` | body | `date` | no | The due date. |
| `subtotal` | body | `number` | no | The subtotal. |
| `tax_rate` | body | `number` | no | The tax rate percentage. |
| `total` | body | `number` | no | The total. |
| `currency` | body | `string` | no | The currency code. |
