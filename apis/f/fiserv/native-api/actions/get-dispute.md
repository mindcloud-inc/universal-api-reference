# Get Dispute with Fiserv

Retrieves detailed dispute information from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/disputes/:id`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Dispute](https://isvportal.fiserv.com/docs/payments-api#operation/get_dispute)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Dispute ID. |
