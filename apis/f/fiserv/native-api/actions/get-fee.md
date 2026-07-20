# Get Fee with Fiserv

Retrieves detailed fee information from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/fees/:id`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Fee](https://isvportal.fiserv.com/docs/payments-api#operation/getOneFeeById)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Fee ID. |
| `x-account-id` | query | `string` | yes | Merchant account ID required in the x-account-id header. |
