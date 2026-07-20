# Get Native Balance for an Address with Etherscan

Retrieves an address's native balance from Etherscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Native Balance for an Address](https://docs.etherscan.io/api-reference/endpoint/balance)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
| `tag` | query | `string` | no |
