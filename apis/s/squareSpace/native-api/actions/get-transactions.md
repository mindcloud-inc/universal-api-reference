# Get Transactions with SquareSpace

Retrieves transactions from Squarespace by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/commerce/transactions/:ids`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Get Transactions](https://developers.squarespace.com/commerce-apis/transactions#get-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Transaction IDs (comma-separated). |
