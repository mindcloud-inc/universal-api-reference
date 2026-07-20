# Get Payment with Fiserv

Retrieves detailed payment information from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments/:id`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Payment](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Payment ID. |
| `x-account-id` | query | `string` | yes | Merchant account ID required in the x-account-id header. |
