# Record Invoice Payment with Quaderno

Records a payment for an invoice in Quaderno.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/:id/payments`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Record Invoice Payment](https://developers.quaderno.io/api/#tag/Invoices/operation/recordInvoicePayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Payment amount. |
| `date` | body | `date` | no | Payment date. |
| `id` | path | `string` | yes | The ID of the invoice to record payment for. |
| `payment_method` | body | `string` | no | Payment method. |
