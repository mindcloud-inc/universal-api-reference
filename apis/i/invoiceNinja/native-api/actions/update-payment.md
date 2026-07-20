# Update Payment with Invoice Ninja

## Endpoint

- **Method:** `PUT`
- **Path:** `/payments/:id`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Update Payment](https://api-docs.invoicing.co/#tag/payments/operation/updatePayment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The payment identifier. |
| `private_notes` | body | `string` | no | Updated internal payment notes. |
| `transaction_reference` | body | `string` | no | Updated transaction reference. |
