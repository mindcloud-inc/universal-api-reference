# Get Balance with Infura Ethereum

Retrieves an address balance from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Balance](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getbalance/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The Ethereum account or contract address to inspect. |
| `params[1]` | body | `string` | yes | The block number or canonical tag to query against. |
