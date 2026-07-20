# Capture Payment Intent with Fiserv

Captures a payment intent in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment_intents/{id}/capture`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Capture Payment Intent](https://isvportal.fiserv.com/docs/payments-api#operation/capture_payment_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment intent id from the path. |
