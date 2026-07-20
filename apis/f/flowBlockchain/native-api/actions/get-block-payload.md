# Get Block Payload with Flow Blockchain

Retrieves a block payload from Flow Blockchain.

## Endpoint

- **Method:** `GET`
- **Path:** `/blocks/{id}/payload`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get Block Payload](https://developers.flow.com/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Block ID whose payload should be returned. |
