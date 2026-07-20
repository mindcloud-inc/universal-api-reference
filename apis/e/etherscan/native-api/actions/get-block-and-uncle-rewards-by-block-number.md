# Get Block and Uncle Rewards by Block Number with Etherscan

Retrieves block and uncle rewards by block number.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Block and Uncle Rewards by Block Number](https://docs.etherscan.io/api-reference/endpoint/getblockreward)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `blockno` | query | `number` | yes |
