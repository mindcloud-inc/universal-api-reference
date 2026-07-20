# Delete Documents By Query with Restdb.io

Deletes documents from Restdb.io by query.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/:collection/*`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Delete Documents By Query](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `q` | query | `string` | yes | JSON query string used to select the documents to delete. |
