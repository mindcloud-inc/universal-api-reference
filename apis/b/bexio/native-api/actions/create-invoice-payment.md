# Create Invoice Payment with Bexio

Creates an invoice payment in Bexio.

## Endpoint

- **Method:** `POST`
- **Path:** `/2.0/kb_invoice/:invoice_id/payment`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Create Invoice Payment](https://docs.bexio.com/#tag/Invoices/operation/v2CreateInvoicePayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | yes | The ID of the invoice. |
| `date` | body | `date` | no | The payment date. |
| `value` | body | `string` | yes | The payment value. |
| `bank_account_id` | body | `number` | no | References a bank account object. |
| `payment_service_id` | body | `number` | no | References a payment service. |
