# Transfer Token with Crossmint

Transfers a token from a Crossmint wallet.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-06-09/wallets/:walletLocator/tokens/:tokenLocator/transfers`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Transfer Token](https://docs.crossmint.com/api-reference/wallets/transfer-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
| `tokenLocator` | path | `string` | yes | Token locator like chain:currency or chain:address. |
| `recipient` | body | `string` | yes | Recipient locator or wallet address. |
| `signer` | body | `string` | no | Optional signer locator. Defaults to the admin signer. |
| `amount` | body | `string` | yes | Decimal token amount to transfer. |
| `transactionType` | body | `string` | no | Transfer transaction type. |
