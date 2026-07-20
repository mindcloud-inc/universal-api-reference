# Get Transaction with Fiserv

Retrieves detailed transaction information from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions/:id`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Transaction](https://isvportal.fiserv.com/docs/payments-api#operation/get_transaction)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Transaction ID. |
| `currency` | query | `list` | no | Currency selector. Accepted values: `0`, `1`. |
