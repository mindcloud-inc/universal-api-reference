# List Transactions with 1Shot

Retrieves transaction records from 1Shot API.

## Endpoint

- **Method:** `GET`
- **Path:** `/business/:businessId/transactions`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [List Transactions](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | The internal UUID of the business. |
| `chainId` | query | `number` | no | — |
| `status` | query | `string` | no | — |
| `walletId` | query | `string` | no | — |
| `contractMethodId` | query | `string` | no | — |
| `apiCredentialId` | query | `string` | no | — |
| `userId` | query | `string` | no | — |
| `memo` | query | `string` | no | — |
| `createdAfter` | query | `date` | no | — |
| `createdBefore` | query | `date` | no | — |
