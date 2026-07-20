# Refund Payment with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/refund`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Refund Payment](https://api-docs.invoicing.co/#tag/payments/operation/storeRefund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The payment to refund. |
| `amount` | body | `number` | yes | Refund amount. |
| `date` | body | `string` | yes | Refund date. |
| `private_notes` | body | `string` | no | Internal refund notes. |
| `invoices` | body | `list<object>` | no | Invoices receiving the refund allocation. |
| `transaction_reference` | body | `string` | no | Refund transaction reference. |
