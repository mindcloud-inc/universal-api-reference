# Create Payment with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/payments`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Create Payment](https://api-docs.invoicing.co/#tag/payments/operation/storePayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | yes | The client receiving the payment. |
| `type_id` | body | `string` | yes | The payment type identifier. |
| `date` | body | `string` | yes | The payment date. |
| `amount` | body | `number` | yes | The payment amount. |
| `invoices` | body | `list<object>` | yes | Invoices to apply the payment to. |
| `transaction_reference` | body | `string` | no | External transaction reference. |
| `private_notes` | body | `string` | no | Internal payment notes. |
