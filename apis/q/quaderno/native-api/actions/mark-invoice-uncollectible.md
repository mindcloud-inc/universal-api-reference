# Mark Invoice Uncollectible with Quaderno

Marks an invoice as uncollectible in Quaderno.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id/mark_uncollectible`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Mark Invoice Uncollectible](https://developers.quaderno.io/api/#tag/Invoices/operation/markInvoiceUncollectible)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the invoice to mark uncollectible. |
