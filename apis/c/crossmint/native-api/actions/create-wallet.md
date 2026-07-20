# Create Wallet with Crossmint

Creates a new wallet in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-06-09/wallets`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Wallet](https://docs.crossmint.com/api-reference/wallets/create-wallet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chainType` | body | `string` | yes | Blockchain type for the wallet. Example: evm. |
| `type` | body | `string` | no | Wallet type. Example: smart. |
| `config.adminSigner.type` | body | `string` | yes | Admin signer type for EVM smart wallets. Example: external-wallet. |
| `config.adminSigner.address` | body | `string` | yes | Admin signer wallet address for EVM smart wallets. |
| `owner` | body | `string` | no | Wallet owner locator such as email:user@example.com or COMPANY. |
| `alias` | body | `string` | no | Optional wallet alias. |
