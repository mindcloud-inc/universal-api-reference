# Create Payment with Fiserv

Creates a payment for a payment intent in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment_intents/{id}/payments`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Create Payment](https://isvportal.fiserv.com/docs/payments-api#operation/create_payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment intent id from the path. |
| `requestBody` | body | `object` | yes | JSON request body from the official create payment schema. |
