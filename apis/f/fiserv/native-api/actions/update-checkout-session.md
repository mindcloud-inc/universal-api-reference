# Update Checkout Session with Fiserv

Updates an existing checkout session in Fiserv.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/checkout_sessions/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Update Checkout Session](https://isvportal.fiserv.com/docs/payments-api#operation/update_checkout_session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Checkout session id from the path. |
| `requestBody` | body | `object` | yes | JSON request body from the official update checkout session schema. |
