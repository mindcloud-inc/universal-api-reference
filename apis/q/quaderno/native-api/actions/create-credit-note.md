# Create Credit Note with Quaderno

Creates a credit note for an invoice in Quaderno.

## Endpoint

- **Method:** `POST`
- **Path:** `/credits`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Create Credit Note](https://developers.quaderno.io/api/#tag/Credits/operation/createCredit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | body | `number` | yes | ID of the invoice to credit. |
| `payment_method` | body | `string` | no | Payment method applied to the credit note. |
| `credited_amount` | body | `number` | no | Partial amount to credit for a single-item invoice. |
