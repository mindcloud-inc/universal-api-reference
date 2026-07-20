# Get EVM Block Transaction Count by Number with Flow Blockchain

Retrieves EVM block transaction count from Flow Blockchain by number.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mainnet.evm.nodes.onflow.org`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get EVM Block Transaction Count by Number](https://developers.flow.com/build/evm/networks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[]` | body | `array<object>` | yes | Ordered JSON-RPC params array: [block number/tag]. |
