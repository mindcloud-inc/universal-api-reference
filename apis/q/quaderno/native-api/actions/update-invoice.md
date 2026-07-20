# Update Invoice with Quaderno

Updates an existing invoice in Quaderno.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Update Invoice](https://developers.quaderno.io/api/#tag/Invoices/operation/updateInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the invoice to update. |
| `notes` | body | `string` | no | Updated invoice notes. |
