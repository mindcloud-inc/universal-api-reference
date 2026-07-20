# List Invoices with Quaderno

Retrieves invoices from Quaderno.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [List Invoices](https://developers.quaderno.io/api/#tag/Invoices/operation/listInvoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | query | `string` | no | Filter invoices by contact ID. |
| `date` | query | `string` | no | Filter invoices by issue date range. |
| `processor_id` | query | `string` | no | Filter invoices by processor ID. |
| `q` | query | `string` | no | Filter invoices by invoice number, customer name, or PO number. |
| `state` | query | `string` | no | Filter invoices by state. |
