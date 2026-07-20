# Get Checkout Session with Fiserv

Retrieves a checkout session from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/checkout_sessions/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Checkout Session](https://isvportal.fiserv.com/docs/payments-api#operation/get_checkout_session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Checkout session id from the path. |
