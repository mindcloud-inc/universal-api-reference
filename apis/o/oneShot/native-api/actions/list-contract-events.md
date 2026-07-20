# List Contract Events with 1Shot

Retrieves contract events from 1Shot API.

## Endpoint

- **Method:** `GET`
- **Path:** `/business/:businessId/events`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [List Contract Events](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | path | `string` | yes | The internal UUID of the business. |
| `chainId` | query | `number` | no | — |
| `name` | query | `string` | no | — |
| `status` | query | `string` | no | — |
| `contractAddress` | query | `string` | no | — |
| `eventName` | query | `string` | no | — |
