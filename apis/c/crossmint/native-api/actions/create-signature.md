# Create Signature with Crossmint

Creates a signature in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-06-09/wallets/:walletLocator/signatures`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Signature](https://docs.crossmint.com/api-reference/wallets/create-signature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
| `type` | body | `string` | yes | Signature type. |
| `params.message` | body | `string` | yes | Message to sign. |
| `params.signer` | body | `string` | yes | Signer identifier used to approve the signature. |
| `params.chain` | body | `string` | yes | Target chain for the signature context. |
