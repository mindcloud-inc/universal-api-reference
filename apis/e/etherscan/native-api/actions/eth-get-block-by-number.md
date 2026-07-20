# eth_getBlockByNumber with Etherscan

Retrieves a block by number from Etherscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [eth_getBlockByNumber](https://docs.etherscan.io/api-reference/endpoint/ethgetblockbynumber)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `tag` | query | `string` | yes |
| `boolean` | query | `boolean` | no |
