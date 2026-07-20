# Get Address ERC721 Token Inventory by Contract with Etherscan

Retrieves ERC721 token inventory by contract for an address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Address ERC721 Token Inventory by Contract](https://docs.etherscan.io/api-reference/endpoint/addresstokennftinventory)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
| `contractaddress` | query | `string` | yes |
| `page` | query | `number` | no |
| `offset` | query | `number` | no |
