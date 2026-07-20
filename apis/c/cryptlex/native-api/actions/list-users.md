# List Users with Cryptlex

Retrieves users from Cryptlex.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/users`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [List Users](https://api.cryptlex.com/v3/docs#tag/Users/operation/get/v3/users)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Number of records per page (1-100). |
| `sort` | query | `string` | no | Sort expression such as -createdAt. |
| `search` | query | `string` | no | Search string. |
