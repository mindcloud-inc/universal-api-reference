# Merge Document with Formstack Documents

Merges data into a document in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.webmerge.me/merge/:id/:key`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Merge Document](https://www.webmerge.me/developers/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `download` | query | `string` | no | Return merged file contents when set to 1 |
| `id` | path | `string` | yes | ID of the document to merge |
| `key` | path | `string` | yes | Merge key from the document URL |
| `test` | query | `string` | no | Use test mode when set to 1 |
