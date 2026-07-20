# List Checkout Sessions with Fiserv

Retrieves checkout sessions for an account from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/checkout_sessions`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Checkout Sessions](https://isvportal.fiserv.com/docs/payments-api#operation/get_checkout_session_list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id to send in the required x-account-id header. |
| `ending_before` | query | `string` | no | Entity id used to page backward through checkout sessions. |
