# List Wallet Transactions with Privy

Retrieves transactions for a wallet from Privy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/wallets/{{walletId}}/transactions`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [List Wallet Transactions](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1{wallet_id}~1transactions/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wallet_id` | path | `string` | yes | Privy wallet ID. |
| `chain` | query | `string` | yes | Blockchain/network to fetch transactions for. |
| `asset` | query | `string` | yes | Asset to fetch transactions for. |
| `tx_hash` | query | `string` | no | Optional transaction hash filter. |
