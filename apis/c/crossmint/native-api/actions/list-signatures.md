# List Signatures with Crossmint

Retrieves signatures from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-06-09/wallets/:walletLocator/signatures`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [List Signatures](https://docs.crossmint.com/api-reference/wallets/get-signatures)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
