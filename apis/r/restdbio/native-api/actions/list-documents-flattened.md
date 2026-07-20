# List Documents Flattened with Restdb.io

Retrieves flattened reference URL fields from Restdb.io documents.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/:collection`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [List Documents Flattened](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `q` | query | `string` | no | JSON query string to filter documents. |
