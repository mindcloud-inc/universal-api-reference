# eth_getBlockTransactionCountByNumber with Etherscan

Retrieves a block transaction count by number.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [eth_getBlockTransactionCountByNumber](https://docs.etherscan.io/api-reference/endpoint/ethgetblocktransactioncountbynumber)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `tag` | query | `string` | yes |
