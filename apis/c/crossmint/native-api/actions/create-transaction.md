# Create Transaction with Crossmint

Creates a transaction in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-06-09/wallets/:walletLocator/transactions`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Transaction](https://docs.crossmint.com/api-reference/wallets/create-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator or wallet address from the Crossmint wallet locator formats. |
| `params.calls[0].to` | body | `string` | yes | Destination address for the EVM call. |
| `params.calls[0].value` | body | `string` | yes | Hex-encoded wei value for the EVM call. |
| `params.calls[0].data` | body | `string` | yes | Hex calldata for the EVM call. |
| `params.chain` | body | `string` | yes | Target EVM chain for the transaction. |
| `params.signer` | body | `string` | yes | Signer identifier used to approve the transaction. |
