# Update Payment Intent with Fiserv

Updates an existing payment intent in Fiserv.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/payment_intents/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Update Payment Intent](https://isvportal.fiserv.com/docs/payments-api#operation/update_payment_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment intent id from the path. |
| `requestBody` | body | `object` | yes | JSON request body from the official update payment intent schema. |
