# Replace Document with Restdb.io

Replaces an existing document in Restdb.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/rest/:collection/:documentId`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Replace Document](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `document` | body | `string` | yes | Full JSON document to replace the existing record. |
| `documentId` | path | `string` | yes | Restdb.io ObjectID of the document. |
