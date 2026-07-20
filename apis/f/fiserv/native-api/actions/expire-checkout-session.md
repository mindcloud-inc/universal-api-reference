# Expire Checkout Session with Fiserv

Expires a checkout session in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/checkout_sessions/{id}/expire`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Expire Checkout Session](https://isvportal.fiserv.com/docs/payments-api#operation/expire_checkout_session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Checkout session id from the path. |
