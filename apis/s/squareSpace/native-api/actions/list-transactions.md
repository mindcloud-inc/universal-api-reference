# List Transactions with SquareSpace

Retrieves transactions from Squarespace.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/commerce/transactions`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [List Transactions](https://developers.squarespace.com/commerce-apis/transactions#list-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedAfter` | query | `date` | no | Return transactions modified after this datetime. |
| `modifiedBefore` | query | `date` | no | Return transactions modified before this datetime. |
