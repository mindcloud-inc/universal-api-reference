# Get Token Info by ContractAddress with Etherscan

Retrieves token information by contract address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Token Info by ContractAddress](https://docs.etherscan.io/api-reference/endpoint/tokeninfo)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `contractaddress` | query | `string` | yes |
