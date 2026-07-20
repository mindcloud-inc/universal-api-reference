# Get Block Number by Timestamp with Etherscan

Retrieves a block number by timestamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Block Number by Timestamp](https://docs.etherscan.io/api-reference/endpoint/getblocknobytime)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `timestamp` | query | `number` | yes |
| `closest` | query | `string` | no |
