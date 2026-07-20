# Get Payment Intent with Fiserv

Retrieves a payment intent from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment_intents/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Payment Intent](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment intent id from the path. |
