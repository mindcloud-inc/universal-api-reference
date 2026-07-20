# Get Account Key with Flow Blockchain

Retrieves an account key from Flow Blockchain.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/{address}/keys/{index}`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get Account Key](https://developers.flow.com/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Flow account address. |
| `index` | path | `string` | yes | Index of the Flow account key. |
