# Update Knowledge Base Document with Docutray

## Endpoint

- **Method:** `PUT`
- **Path:** `api/knowledge-bases/:id/documents/:documentId`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Update Knowledge Base Document](https://docs.docutray.com/docs/operations/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Unique ID of the document |
| `id` | path | `string` | yes | Unique ID of the Knowledge Base |
| `content` | body | `object` | no | New document content |
| `metadata` | body | `object` | no | Updated metadata |
| `regenerateEmbedding` | body | `boolean` | no | Force embedding regeneration |
