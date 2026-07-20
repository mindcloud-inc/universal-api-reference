# Get Top Token Holders with Etherscan

Retrieves the top token holders for a contract.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Top Token Holders](https://docs.etherscan.io/api-reference/endpoint/toptokenholders)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `contractaddress` | query | `string` | yes |
| `offset` | query | `number` | no |
