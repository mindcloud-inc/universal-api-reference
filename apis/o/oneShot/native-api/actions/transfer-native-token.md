# Transfer Native Token with 1Shot

Creates a native token transfer from a 1Shot API wallet.

## Endpoint

- **Method:** `POST`
- **Path:** `/wallets/:walletId/transfer`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Transfer Native Token](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `walletId` | path | `string` | yes |
| `destinationAccountAddress` | body | `string` | yes |
| `transferAmount` | body | `string` | no |
| `memo` | body | `string` | no |
