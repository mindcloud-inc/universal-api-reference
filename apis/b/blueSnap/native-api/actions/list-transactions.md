# List Transactions with BlueSnap

Retrieves transactions from BlueSnap.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions`
- **Base URL:** `https://sandbox.bluesnap.com/services/2`
- **Official documentation:** [List Transactions](https://developers.bluesnap.com/v8976-JSON/reference/retrieve)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pagesize` | query | `string` | no | Number of results to return. |
| `gettotal` | query | `boolean` | no | Whether to include total results count. |
| `merchantTransactionId` | query | `string` | no | Filter by merchant transaction ID, if supported. |
| `after` | query | `string` | no | Return transactions after this transaction ID. |
| `before` | query | `string` | no | Return transactions before this transaction ID. |
