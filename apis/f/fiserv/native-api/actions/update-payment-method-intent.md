# Update Payment Method Intent with Fiserv

Updates an existing payment method intent in Fiserv.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/payment_method_intents/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Update Payment Method Intent](https://isvportal.fiserv.com/docs/payments-api#operation/update_payment_method_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment method intent id from the path. |
| `requestBody` | body | `object` | yes | JSON request body from the official update payment method intent schema. |
