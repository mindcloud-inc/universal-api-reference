# Advanced Search Knowledge Base with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/knowledge-bases/:id/search`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Advanced Search Knowledge Base](https://docs.docutray.com/docs/operations/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of the Knowledge Base |
| `query` | body | `string` | yes | Search query |
| `limit` | body | `number` | no | Maximum number of results |
| `similarityThreshold` | body | `number` | no | Minimum similarity threshold |
| `includeMetadata` | body | `boolean` | no | Include metadata in results |
