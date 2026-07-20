# Get Transaction By Hash with Infura Ethereum

Retrieves a transaction from Infura Ethereum by hash.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Transaction By Hash](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gettransactionbyhash/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The transaction hash to retrieve. |
