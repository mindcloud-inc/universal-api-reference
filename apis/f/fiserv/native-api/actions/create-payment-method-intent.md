# Create Payment Method Intent with Fiserv

Creates a payment method intent in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment_method_intents`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Create Payment Method Intent](https://isvportal.fiserv.com/docs/payments-api#operation/create_payment_method_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `requestBody` | body | `object` | yes | JSON request body from the official create payment method intent schema. |
