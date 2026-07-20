# Update Wallet with Privy

Updates an existing wallet in Privy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/wallets/{{walletId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Update Wallet](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1{wallet_id}/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wallet_id` | path | `string` | yes | Privy wallet ID. |
