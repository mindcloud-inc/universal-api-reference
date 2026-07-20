# Get Data Account Transactions with TrueLayer

Retrieves data account transactions from TrueLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/v1/accounts/:account_id/transactions`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Get Data Account Transactions](https://docs.truelayer.com/docs/account-and-card-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | TrueLayer Data API account ID. |
