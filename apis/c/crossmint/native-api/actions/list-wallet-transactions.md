# List Wallet Transactions with Crossmint

Retrieves wallet transactions from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-06-09/wallets/:walletLocator/transactions`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [List Wallet Transactions](https://docs.crossmint.com/api-reference/wallets/get-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
