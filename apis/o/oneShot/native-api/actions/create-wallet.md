# Create Wallet with 1Shot

Creates a new wallet in 1Shot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/:businessId/wallets`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Create Wallet](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `businessId` | path | `string` | yes |
| `chainId` | body | `number` | yes |
| `name` | body | `string` | yes |
