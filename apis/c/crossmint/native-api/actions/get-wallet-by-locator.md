# Get Wallet By Locator with Crossmint

Retrieves a wallet from Crossmint by locator.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-06-09/wallets/:walletLocator`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Get Wallet By Locator](https://docs.crossmint.com/api-reference/wallets/get-wallet-by-locator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
