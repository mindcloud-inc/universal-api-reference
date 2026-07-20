# Get Payment Method Intent with Fiserv

Retrieves a payment method intent from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment_method_intents/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Payment Method Intent](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_method_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment method intent id from the path. |
