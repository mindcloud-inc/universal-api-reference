# eth_getTransactionCount with Etherscan

Retrieves an address transaction count from Etherscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [eth_getTransactionCount](https://docs.etherscan.io/api-reference/endpoint/ethgettransactioncount)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
| `tag` | query | `string` | no |
