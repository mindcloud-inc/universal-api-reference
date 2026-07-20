# List Transactions with Fiserv

Retrieves transactions for an account from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Transactions](https://isvportal.fiserv.com/docs/payments-api#operation/get_transactions)

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
| `payout_id` | query | `string` | no | Filter transactions by payout ID. |
| `starting_after` | query | `string` | no | Cursor ID to start after. |
| `limit` | query | `number` | no | Maximum number of transactions to return. |
| `currency` | query | `list` | no | Filter transactions by currency. Accepted values: `0`, `1`. |
