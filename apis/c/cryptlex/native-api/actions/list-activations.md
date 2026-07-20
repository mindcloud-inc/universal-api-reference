# List Activations with Cryptlex

Retrieves activations from Cryptlex.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/activations`
- **Base URL:** `https://api.cryptlex.com`
- **Official documentation:** [List Activations](https://api.cryptlex.com/v3/docs#tag/Activations/operation/get/v3/activations)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Number of records per page (1-100). |
| `sort` | query | `string` | no | Sort expression such as -createdAt. |
| `search` | query | `string` | no | Search string. |
