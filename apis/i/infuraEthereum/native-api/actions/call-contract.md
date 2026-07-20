# Call Contract with Infura Ethereum

Retrieves a contract call result from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Call Contract](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_call/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0][data]` | body | `string` | yes | ABI-encoded function selector and arguments for the contract call. |
| `params[0][to]` | body | `string` | yes | The target contract address for the read-only call. |
| `params[1]` | body | `string` | yes | The block number or canonical tag to query against. |
