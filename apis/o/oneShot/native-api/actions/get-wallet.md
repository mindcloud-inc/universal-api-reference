# Get Wallet with 1Shot

Retrieves wallet details from 1Shot API.

## Endpoint

- **Method:** `GET`
- **Path:** `/wallets/:walletId`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Get Wallet](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletId` | path | `string` | yes | The internal UUID of the wallet. |
| `includeBalances` | query | `boolean` | no | — |
