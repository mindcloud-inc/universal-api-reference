# Get Transaction By Block Number And Index with Infura Ethereum

Retrieves a transaction from Infura Ethereum by block and index.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Transaction By Block Number And Index](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gettransactionbyblocknumberandindex/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The block number as a hex quantity. |
| `params[1]` | body | `string` | yes | The transaction index within the block as a hex quantity. |
