# Create Child Document with Restdb.io

Creates a child document in Restdb.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/:collection/:documentId/:childField`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Create Child Document](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `childField` | path | `string` | yes | Child field name on the parent document. |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `document` | body | `string` | yes | JSON child document to create. |
| `documentId` | path | `string` | yes | Restdb.io ObjectID of the parent document. |
