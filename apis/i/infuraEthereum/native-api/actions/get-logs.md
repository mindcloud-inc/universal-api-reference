# Get Logs with Infura Ethereum

Retrieves logs from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Logs](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getlogs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0][address]` | body | `string` | yes | Filter logs to one contract address. |
| `params[0][fromBlock]` | body | `string` | yes | The starting block number or tag for the log search. |
| `params[0][toBlock]` | body | `string` | yes | The ending block number or tag for the log search. |
