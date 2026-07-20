# Get ERC1155 Token Transfers by Address with Etherscan

Retrieves ERC1155 token transfers for an address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get ERC1155 Token Transfers by Address](https://docs.etherscan.io/api-reference/endpoint/token1155tx)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `contractaddress` | query | `string` | no |
| `address` | query | `string` | yes |
| `startblock` | query | `number` | no |
| `endblock` | query | `number` | no |
| `page` | query | `number` | no |
| `offset` | query | `number` | no |
| `sort` | query | `string` | no |
