# Get Signature with Crossmint

Retrieves a signature from Crossmint.

## Endpoint

- **Method:** `GET`
- **Path:** `/2025-06-09/wallets/:walletLocator/signatures/:signatureId`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [Get Signature](https://docs.crossmint.com/api-reference/wallets/get-signature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletLocator` | path | `string` | yes | Wallet locator using the Crossmint wallet locator formats. |
| `signatureId` | path | `string` | yes | Signature identifier returned by Crossmint. |
