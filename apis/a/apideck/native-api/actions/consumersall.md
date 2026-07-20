# Get all consumers with Apideck

Retrieves all consumers from Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/consumers`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Get all consumers](https://developers.apideck.com/apis/vault/reference/consumers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `object` | no | — |
| `cursor` | query | `string` | no | Cursor to start from for the next page. |
| `limit` | query | `number` | no | Number of results to return. Minimum 1, maximum 200. |
