# Get Wallet with Privy

Retrieves a wallet from Privy by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/wallets/{{walletId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Get Wallet](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1{wallet_id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wallet_id` | path | `string` | yes | Privy wallet ID. |
