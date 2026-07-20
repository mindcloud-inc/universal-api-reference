# Patch Document with Restdb.io

Updates selected fields on a Restdb.io document.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/:collection/:documentId`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Patch Document](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `documentId` | path | `string` | yes | Restdb.io ObjectID of the document. |
| `patch` | body | `string` | yes | JSON object with the properties to update. |
