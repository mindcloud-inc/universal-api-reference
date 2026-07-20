# List Contract Methods with 1Shot

Retrieves contract method endpoints from 1Shot API.

## Endpoint

- **Method:** `GET`
- **Path:** `/business/:businessId/methods`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [List Contract Methods](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | The internal UUID of the business. |
| `chainId` | query | `number` | no | — |
| `name` | query | `string` | no | — |
| `status` | query | `string` | no | — |
| `contractAddress` | query | `string` | no | — |
| `promptId` | query | `string` | no | — |
| `methodType` | query | `string` | no | — |
