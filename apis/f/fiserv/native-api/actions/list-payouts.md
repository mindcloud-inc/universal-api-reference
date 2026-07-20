# List Payouts with Fiserv

Retrieves payouts for an account from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payouts`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Payouts](https://isvportal.fiserv.com/docs/payments-api#operation/get_payouts)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ending_before` | query | `string` | no | Cursor ID to end before. |
| `starting_after` | query | `string` | no | Cursor ID to start after. |
| `limit` | query | `number` | no | Maximum number of payouts to return. |
| `status` | query | `list` | no | Payout status filter. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
