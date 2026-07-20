# Delete Memory Document with Langbase

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1/memory/:memoryName/documents/:documentName`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Delete Memory Document](https://langbase.com/docs/api-reference/memory/document-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memoryName` | path | `string` | yes | Memory name that owns the document. |
| `documentName` | path | `string` | yes | Document name to delete. |
