# Retry Memory Document Embeddings with Langbase

## Endpoint

- **Method:** `GET`
- **Path:** `v1/memory/:memoryName/documents/:documentName/embeddings/retry`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Retry Memory Document Embeddings](https://langbase.com/docs/api-reference/memory/document-embeddings-retry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memoryName` | path | `string` | yes | Memory name that owns the document. |
| `documentName` | path | `string` | yes | Document name to retry embeddings for. |
