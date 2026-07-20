# Get Transaction By Reference ID with Privy

Finds transactions in Privy by reference ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transactions`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Get Transaction By Reference ID](https://api.privy.io/v1/openapi.json#/paths/~1v1~1transactions/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference_id` | query | `string` | yes | External reference ID for transaction lookup. |
