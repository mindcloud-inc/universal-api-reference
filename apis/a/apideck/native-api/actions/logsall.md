# Get all consumer request logs with Apideck

Retrieves consumer request logs from Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/logs`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Get all consumer request logs](https://developers.apideck.com/apis/vault/reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter` | query | `object` | no |
| `cursor` | query | `string` | no |
| `limit` | query | `number` | no |
