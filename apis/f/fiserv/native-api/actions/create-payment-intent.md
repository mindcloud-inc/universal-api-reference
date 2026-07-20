# Create Payment Intent with Fiserv

Creates a payment intent in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment_intents`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Create Payment Intent](https://isvportal.fiserv.com/docs/payments-api#operation/create_payment_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `requestBody` | body | `object` | yes | JSON request body from the official create payment intent schema. |
