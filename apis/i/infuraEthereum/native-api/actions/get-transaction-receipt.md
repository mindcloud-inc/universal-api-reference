# Get Transaction Receipt with Infura Ethereum

Retrieves a transaction receipt from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Transaction Receipt](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_gettransactionreceipt/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The transaction hash to inspect. |
