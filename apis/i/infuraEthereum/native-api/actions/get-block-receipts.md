# Get Block Receipts with Infura Ethereum

Retrieves block receipts from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Block Receipts](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getblockreceipts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The block number or block hash to retrieve receipts for. |
