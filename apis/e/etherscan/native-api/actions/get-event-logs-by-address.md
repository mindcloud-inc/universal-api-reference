# Get Event Logs by Address with Etherscan

Retrieves event logs for an address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Event Logs by Address](https://docs.etherscan.io/api-reference/endpoint/getlogs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
| `fromBlock` | query | `number` | no |
| `toBlock` | query | `number` | no |
| `page` | query | `number` | no |
| `offset` | query | `number` | no |
