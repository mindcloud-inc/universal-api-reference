# Get ERC20-Token Account Balance for Token Contract Address with Etherscan

Retrieves an ERC20 token balance for an address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get ERC20-Token Account Balance for Token Contract Address](https://docs.etherscan.io/api-reference/endpoint/tokenbalance)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `contractaddress` | query | `string` | yes |
| `address` | query | `string` | yes |
| `tag` | query | `string` | no |
