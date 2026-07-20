# List Transactions with Bridge

Retrieves transactions from Bridge.

## Endpoint

- **Method:** `GET`
- **Path:** `/aggregation/transactions`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [List Transactions](https://docs.bridgeapi.io/reference/gettransactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAccessToken` | body | `string` | yes | Bridge user access token returned by the Authorization token action. |
| `account_id` | query | `number` | no | Filter transactions by account |
| `since` | query | `date` | no | Limit transactions to those with an `updated_at` value after the specified timestamp |
| `until` | query | `date` | no | Limit transactions to those with an `updated_at` value before the specified timestamp |
| `min_date` | query | `date` | no | Limit transactions to those with a `date` value after the specified date |
| `max_date` | query | `date` | no | Limit transactions to those with a `date` value before the specified date |
