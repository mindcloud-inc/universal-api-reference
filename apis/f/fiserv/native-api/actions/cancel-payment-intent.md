# Cancel Payment Intent with Fiserv

Cancels a payment intent in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment_intents/{id}/cancel`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Cancel Payment Intent](https://isvportal.fiserv.com/docs/payments-api#operation/cancel_payment_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment intent id from the path. |
