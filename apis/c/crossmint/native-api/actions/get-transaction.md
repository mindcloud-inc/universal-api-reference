# Get Transaction with Crossmint

Retrieves a transaction from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-06-09/wallets/:walletLocator/transactions/:transactionId`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Get Transaction](https://docs.crossmint.com/api-reference/wallets/get-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
| `transactionId` | path | `string` | yes | Transaction identifier returned by Crossmint. |
