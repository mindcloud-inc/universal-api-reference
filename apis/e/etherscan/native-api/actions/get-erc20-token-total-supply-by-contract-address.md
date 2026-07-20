# Get ERC20-Token TotalSupply by Contract Address with Etherscan

Retrieves an ERC20 token total supply by contract.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get ERC20-Token TotalSupply by Contract Address](https://docs.etherscan.io/etherscan-v2/api-endpoints/tokens)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `contractaddress` | query | `string` | yes |
