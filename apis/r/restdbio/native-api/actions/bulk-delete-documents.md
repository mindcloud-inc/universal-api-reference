# Bulk Delete Documents with Restdb.io

Deletes multiple documents from Restdb.io by ID list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/:collection/*`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Bulk Delete Documents](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `ids` | body | `string` | yes | Array of Restdb.io ObjectIDs to delete. |
