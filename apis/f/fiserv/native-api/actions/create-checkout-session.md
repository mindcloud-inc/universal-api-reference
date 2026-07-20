# Create Checkout Session with Fiserv

Creates a checkout session in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/checkout_sessions`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Create Checkout Session](https://isvportal.fiserv.com/docs/payments-api#operation/create_checkout_session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `requestBody` | body | `object` | yes | JSON request body from the official create checkout session schema. |
