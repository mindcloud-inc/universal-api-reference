# Get EVM Block Receipts with Flow Blockchain

Retrieves EVM block receipts from Flow Blockchain.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mainnet.evm.nodes.onflow.org`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get EVM Block Receipts](https://developers.flow.com/build/evm/networks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[]` | body | `array<object>` | yes | Ordered JSON-RPC params array: [block number/tag or block hash]. |
