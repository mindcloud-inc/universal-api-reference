# Get EVM Fee History with Flow Blockchain

Retrieves EVM fee history from Flow Blockchain.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mainnet.evm.nodes.onflow.org`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get EVM Fee History](https://developers.flow.com/build/evm/networks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[]` | body | `array<object>` | yes | Ordered JSON-RPC params array: [block count, newest block, reward percentiles]. |
