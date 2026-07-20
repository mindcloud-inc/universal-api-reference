# eth_getTransactionByHash with Etherscan

Retrieves a transaction by hash from Etherscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [eth_getTransactionByHash](https://docs.etherscan.io/api-reference/endpoint/ethgettransactionbyhash)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `txhash` | query | `string` | yes |
