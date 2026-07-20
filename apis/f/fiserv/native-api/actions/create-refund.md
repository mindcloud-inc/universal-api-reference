# Create Refund with Fiserv

Creates a refund for a payment intent in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment_intents/{id}/refunds`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Create Refund](https://isvportal.fiserv.com/docs/payments-api#operation/create_refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment intent id from the path. |
| `requestBody` | body | `object` | yes | JSON request body from the official create refund schema. |
