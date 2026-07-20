# Get Fee History with Infura Ethereum

Retrieves fee history from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Fee History](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_feehistory/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | How many recent blocks to include, as a hex quantity. |
| `params[1]` | body | `string` | yes | The newest block to anchor the history window, such as latest or a hex block number. |
