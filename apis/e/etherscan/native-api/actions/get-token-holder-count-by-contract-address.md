# Get Token Holder Count by Contract Address with Etherscan

Retrieves the token holder count for a contract.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Token Holder Count by Contract Address](https://docs.etherscan.io/api-reference/endpoint/tokenholdercount)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `contractaddress` | query | `string` | yes |
