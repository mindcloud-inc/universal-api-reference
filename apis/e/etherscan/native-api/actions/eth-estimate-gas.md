# eth_estimateGas with Etherscan

Retrieves an estimated gas usage for a transaction.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [eth_estimateGas](https://docs.etherscan.io/api-reference/endpoint/ethestimategas)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `data` | query | `string` | no |
| `to` | query | `string` | yes |
| `value` | query | `string` | no |
| `gasPrice` | query | `string` | no |
| `gas` | query | `string` | no |
