# Get Document with Restdb.io

Retrieves a document from Restdb.io by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/:collection/:documentId`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Get Document](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `documentId` | path | `string` | yes | Restdb.io ObjectID of the document. |
