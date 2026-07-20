# Inspect Contract with 1Shot

Retrieves contract details from 1Shot API.

## Endpoint

- **Method:** `GET`
- **Path:** `/chains/:chainId/contracts/:contractAddress`
- **Base URL:** `https://api.1shotapi.com/v0`
- **Official documentation:** [Inspect Contract](https://docs.1shotapi.com/api/openapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chainId` | path | `string` | yes | The chain identifier. |
| `contractAddress` | path | `string` | yes | The contract address to inspect. |
