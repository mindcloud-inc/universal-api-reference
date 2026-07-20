# Create Contract Event with 1Shot

Creates a new contract event in 1Shot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/:businessId/events`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Create Contract Event](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `businessId` | path | `string` | yes |
| `chainId` | body | `number` | yes |
| `contractAddress` | body | `string` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | yes |
| `eventName` | body | `string` | yes |
