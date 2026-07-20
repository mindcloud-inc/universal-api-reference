# Create Invoice with Quaderno

Creates a new invoice in Quaderno.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Create Invoice](https://developers.quaderno.io/api/#tag/Invoices/operation/createInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | yes | Existing contact ID or contact object. |
| `currency` | body | `string` | no | Invoice currency code. |
| `notes` | body | `string` | no | Invoice notes. |
| `items[]` | body | `array<object>` | yes | Invoice line items array. |
| `issue_date` | body | `date` | no | Invoice issue date. |
| `due_date` | body | `date` | no | Invoice due date. |
