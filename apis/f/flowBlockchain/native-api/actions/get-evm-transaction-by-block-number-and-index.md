# Get EVM Transaction by Block Number and Index with Flow Blockchain

Retrieves an EVM transaction from Flow Blockchain by block number and index.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mainnet.evm.nodes.onflow.org`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get EVM Transaction by Block Number and Index](https://developers.flow.com/build/evm/networks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[]` | body | `array<object>` | yes | Ordered JSON-RPC params array: [block number/tag, transaction index]. |
