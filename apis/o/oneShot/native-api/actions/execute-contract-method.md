# Execute Contract Method with 1Shot

Creates a blockchain transaction from a contract method in 1Shot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/methods/:contractMethodId/execute`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Execute Contract Method](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contractMethodId` | path | `string` | yes |
| `params` | body | `object` | no |
