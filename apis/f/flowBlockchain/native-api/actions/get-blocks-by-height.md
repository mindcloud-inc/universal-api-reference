# Get Blocks by Height with Flow Blockchain

Retrieves blocks from Flow Blockchain by height.

## Endpoint

- **Method:** `GET`
- **Path:** `/blocks`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get Blocks by Height](https://developers.flow.com/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `height` | query | `string` | no | Block height or height alias to fetch. Incompatible with start and end height. |
