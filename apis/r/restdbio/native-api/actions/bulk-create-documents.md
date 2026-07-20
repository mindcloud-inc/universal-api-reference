# Bulk Create Documents with Restdb.io

Creates multiple documents in Restdb.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/:collection`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Bulk Create Documents](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | path | `string` | yes | Collection name in the target Restdb.io database. |
| `documents` | body | `string` | yes | Array of JSON documents to insert. |
