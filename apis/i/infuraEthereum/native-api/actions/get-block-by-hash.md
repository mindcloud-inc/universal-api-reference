# Get Block By Hash with Infura Ethereum

Retrieves a block from Infura Ethereum by hash.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Block By Hash](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getblockbyhash/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The block hash to retrieve. |
| `params[1]` | body | `boolean` | yes | Whether to expand transactions to full objects instead of transaction hashes. |
