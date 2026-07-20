# Get Wallet Balance with Privy

Retrieves a wallet balance from Privy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/wallets/{{walletId}}/balance`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Get Wallet Balance](https://api.privy.io/v1/openapi.json#/paths/~1v1~1wallets~1{wallet_id}~1balance/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wallet_id` | path | `string` | yes | Privy wallet ID. |
| `asset` | query | `string` | no | Optional asset filter for the balance request. |
| `chain` | query | `string` | no | Optional chain filter for the balance request. |
| `include_currency` | query | `string` | no | Optional fiat currency code to include valuation data. |
