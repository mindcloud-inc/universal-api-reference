# Copy Document with Formstack Documents

Creates a copy of a document in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:id/copy`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Copy Document](https://www.webmerge.me/developers/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the document to copy |
| `name` | body | `string` | yes | Name of the copied document |
