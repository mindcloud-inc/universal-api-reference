# Get Internal Transactions by Address with Etherscan

Retrieves internal transactions for an address.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/api`
- **Base URL:** `https://api.etherscan.io`
- **Official documentation:** [Get Internal Transactions by Address](https://docs.etherscan.io/api-reference/endpoint/txlistinternal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chainid` | query | `string` | no |
| `address` | query | `string` | yes |
| `startblock` | query | `number` | no |
| `endblock` | query | `number` | no |
| `page` | query | `number` | no |
| `offset` | query | `number` | no |
| `sort` | query | `string` | no |
