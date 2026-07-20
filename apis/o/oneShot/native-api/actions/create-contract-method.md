# Create Contract Method with 1Shot

Creates a new contract method endpoint in 1Shot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/:businessId/methods`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Create Contract Method](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `businessId` | path | `string` | yes |
| `chainId` | body | `number` | yes |
| `contractAddress` | body | `string` | yes |
| `walletId` | body | `string` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | yes |
| `functionName` | body | `string` | yes |
| `stateMutability` | body | `string` | yes |
| `inputs` | body | `list<object>` | yes |
