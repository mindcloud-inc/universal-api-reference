# Create Access List with Infura Ethereum

Retrieves an access list from Infura Ethereum.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/:apiKey`
- **Base URL:** `https://mainnet.infura.io`
- **Official documentation:** [Create Access List](https://docs.metamask.io/services/reference/ethereum/json-rpc-methods/eth_createaccesslist/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params[0][data]` | body | `string` | yes | ABI-encoded function selector and arguments used for access-list generation. |
| `params[0][to]` | body | `string` | yes | The target contract or recipient address for the access-list simulation. |
| `params[1]` | body | `string` | yes | The block number or canonical tag to simulate against. |
