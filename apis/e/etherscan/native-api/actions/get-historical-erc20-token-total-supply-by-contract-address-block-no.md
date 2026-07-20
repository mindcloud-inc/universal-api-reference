# Get Historical ERC20-Token TotalSupply by ContractAddress & BlockNo with Etherscan

Retrieves historical ERC20 token total supply by block.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Historical ERC20-Token TotalSupply by ContractAddress & BlockNo](https://docs.etherscan.io/api-reference/endpoint/tokensupplyhistory)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `contractaddress` | query | `string` | yes |
| `blockno` | query | `number` | yes |
