# Deliver Invoice with Quaderno

Delivers an invoice to the customer by email in Quaderno.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:id/deliver`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Deliver Invoice](https://developers.quaderno.io/api/#tag/Invoices/operation/deliverInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the invoice to deliver. |
