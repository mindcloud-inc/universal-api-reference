# List Wallet Transfers with Crossmint

Retrieves wallet transfer activity from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/unstable/wallets/:walletLocator/transfers`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [List Wallet Transfers](https://docs.crossmint.com/api-reference/wallets/list-transfers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
| `chain` | query | `string` | yes | Blockchain network to query. |
| `tokens` | query | `string` | yes | Comma-separated list of tokens or token locator strings. |
| `status` | query | `string` | yes | Transfer status to query. |
