# Cancel Payment Method Intent with Fiserv

Cancels a payment method intent in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment_method_intents/{id}/cancel`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Cancel Payment Method Intent](https://isvportal.fiserv.com/docs/payments-api#operation/cancel_payment_method_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment method intent id from the path. |
