# List Releases with Cryptlex

Retrieves releases from Cryptlex.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/releases`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [List Releases](https://api.cryptlex.com/v3/docs#tag/Releases/operation/get/v3/releases)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Number of records per page (1-100). |
| `sort` | query | `string` | no | Sort expression such as -createdAt. |
| `search` | query | `string` | no | Search string. |
