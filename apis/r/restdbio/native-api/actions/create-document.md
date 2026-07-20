# Create Document with Restdb.io

Creates a new document in Restdb.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/:collection`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Create Document](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `document` | body | `string` | yes | JSON document to create in the target collection. |
