# List Wallets with 1Shot

Retrieves wallet records from 1Shot API.

## Endpoint

- **Method:** `GET`
- **Path:** `/business/:businessId/wallets`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [List Wallets](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | The internal UUID of the business. |
| `chainId` | query | `number` | no | — |
| `name` | query | `string` | no | — |
