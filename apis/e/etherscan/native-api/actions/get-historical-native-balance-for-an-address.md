# Get Historical Native Balance for an Address with Etherscan

Retrieves an address's historical native balance from Etherscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Historical Native Balance for an Address](https://docs.etherscan.io/api-reference/endpoint/balancehistory)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
| `blockno` | query | `number` | yes |
