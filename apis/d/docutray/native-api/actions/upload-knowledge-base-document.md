# Upload Knowledge Base Document with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/knowledge-bases/:id/documents`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Upload Knowledge Base Document](https://docs.docutray.com/docs/operations/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of the Knowledge Base |
| `documentId` | body | `string` | yes | Unique document ID |
| `content` | body | `object` | yes | Document content in JSON format |
| `metadata` | body | `object` | no | Additional document metadata |
| `generateEmbedding` | body | `boolean` | no | Automatically generate embedding |
