# Get Block Transaction Count By Number with Infura Ethereum

Retrieves block transaction count from Infura Ethereum by number.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Get Block Transaction Count By Number](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_getblocktransactioncountbynumber/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0]` | body | `string` | yes | The block number or canonical tag to query against. |
