# Get Contract ABI with Etherscan

Retrieves a contract ABI from Etherscan.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Contract ABI](https://docs.etherscan.io/api-reference/endpoint/getabi)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
