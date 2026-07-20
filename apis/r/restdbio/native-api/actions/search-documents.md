# Search Documents with Restdb.io

Finds documents in Restdb.io by text search.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/:collection`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Search Documents](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `filter` | query | `string` | yes | Text search string used by Restdb.io's filter parameter. |
