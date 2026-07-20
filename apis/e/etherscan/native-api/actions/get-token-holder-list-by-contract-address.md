# Get Token Holder List by Contract Address with Etherscan

Retrieves the token holder list for a contract.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Token Holder List by Contract Address](https://docs.etherscan.io/api-reference/endpoint/tokenholderlist)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `contractaddress` | query | `string` | yes |
| `page` | query | `number` | no |
| `offset` | query | `number` | no |
