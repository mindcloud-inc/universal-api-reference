# Get Address ERC20 Token Holding with Etherscan

Retrieves ERC20 token holdings for an address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Address ERC20 Token Holding](https://docs.etherscan.io/api-reference/endpoint/addresstokenbalance)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
| `page` | query | `number` | no |
| `offset` | query | `number` | no |
