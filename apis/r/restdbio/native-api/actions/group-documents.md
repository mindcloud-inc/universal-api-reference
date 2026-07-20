# Group Documents with Restdb.io

Retrieves documents grouped by a Restdb.io field.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/:collection`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Group Documents](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `groupby` | query | `string` | yes | Field name to group by. |
