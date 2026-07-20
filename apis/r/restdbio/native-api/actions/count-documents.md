# Count Documents with Restdb.io

Retrieves document counts from a Restdb.io collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/:collection`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Count Documents](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `q` | query | `string` | no | JSON query string to count matching documents only. |
