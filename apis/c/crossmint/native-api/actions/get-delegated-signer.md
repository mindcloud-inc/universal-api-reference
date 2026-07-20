# Get Delegated Signer with Crossmint

Retrieves a delegated signer from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-06-09/wallets/:walletLocator/signers/:signer`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Get Delegated Signer](https://docs.crossmint.com/api-reference/wallets/get-signer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
| `signer` | path | `string` | yes | Signer locator. |
