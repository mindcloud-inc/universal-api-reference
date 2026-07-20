# Get Block By Number with Infura Ethereum

Retrieves a block from Infura Ethereum by number.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Block By Number](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getblockbynumber/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The block number or canonical tag to retrieve. |
| `params[1]` | body | `boolean` | yes | Whether to expand transactions to full objects instead of transaction hashes. |
