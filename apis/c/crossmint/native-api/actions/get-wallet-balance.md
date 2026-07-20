# Get Wallet Balance with Crossmint

Retrieves a wallet balance from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-06-09/wallets/:walletLocator/balances`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Get Wallet Balance](https://docs.crossmint.com/api-reference/wallets/get-wallet-balance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
| `tokens` | query | `string` | yes | Comma-separated list of tokens or token locators to query. |
| `chains` | query | `string` | no | Optional comma-separated list of chains to query. |
