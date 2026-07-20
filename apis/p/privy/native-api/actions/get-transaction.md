# Get Transaction with Privy

Retrieves a transaction from Privy by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transactions/{{transactionId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Get Transaction](https://api.privy.io/v1/openapi.json#/paths/~1v1~1transactions~1{transaction_id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `string` | yes | Privy transaction ID. |
