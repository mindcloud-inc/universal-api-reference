# Get Payout with Fiserv

Retrieves detailed payout information from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payouts/:id`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Payout](https://isvportal.fiserv.com/docs/payments-api#operation/get_payout)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Payout ID. |
| `ledger_type` | query | `list` | no | Filter payout by ledger type. Accepted values: `0`, `1`. |
| `currency` | query | `list` | no | Currency selector. Accepted values: `0`, `1`. |
| `x-account-id` | query | `string` | no | Optional account ID sent in x-account-id when fetching an account payout. |
