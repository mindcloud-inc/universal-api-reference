# Create Delegated Signer with Crossmint

Creates a delegated signer in Crossmint.

## Endpoint

- **Method:** `POST`
- **Path:** `/2025-06-09/wallets/:walletLocator/signers`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Create Delegated Signer](https://docs.crossmint.com/api-reference/wallets/register-delegated-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
| `signer` | body | `string` | yes | Signer to register as a delegated signer. |
| `chain` | body | `string` | yes | Chain where the signer will be registered. |
| `expiresAt` | body | `string` | no | Optional ISO 8601 expiry time for the signer. |
