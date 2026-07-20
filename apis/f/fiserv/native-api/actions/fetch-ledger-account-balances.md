# Fetch Ledger Account Balances with Fiserv

Retrieves ledger account balances from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/balances`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Fetch Ledger Account Balances](https://isvportal.fiserv.com/docs/payments-api#operation/get_ledger_account_balances)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ledger_type` | query | `list` | no | Filter balances by ledger type. Accepted values: `0`, `1`. |
| `currency` | query | `list` | no | Filter balances by currency. Accepted values: `0`, `1`. |
