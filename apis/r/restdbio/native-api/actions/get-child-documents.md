# Get Child Documents with Restdb.io

Retrieves child documents from a Restdb.io record.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/:collection/:documentId/:childField`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Get Child Documents](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `childField` | path | `string` | yes | Child field name on the parent document. |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `documentId` | path | `string` | yes | Restdb.io ObjectID of the parent document. |
