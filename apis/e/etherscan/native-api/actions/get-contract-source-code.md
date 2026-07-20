# Get Contract Source Code with Etherscan

Retrieves a contract source code record from Etherscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Contract Source Code](https://docs.etherscan.io/api-reference/endpoint/getsourcecode)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
