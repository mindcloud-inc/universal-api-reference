# Get Child Document with Restdb.io

Retrieves a child document from Restdb.io by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/:collection/:documentId/:childField/:childDocumentId`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Get Child Document](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `childDocumentId` | path | `string` | yes | Restdb.io ObjectID of the child document. |
| `childField` | path | `string` | yes | Child field name on the parent document. |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `documentId` | path | `string` | yes | Restdb.io ObjectID of the parent document. |
