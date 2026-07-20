# Get Transaction Count with Infura Ethereum

Retrieves an address transaction count from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Transaction Count](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gettransactioncount/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The Ethereum account or contract address to inspect. |
| `params[1]` | body | `string` | yes | The block number or canonical tag to query against. |
