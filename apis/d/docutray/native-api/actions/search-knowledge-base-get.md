# Search Knowledge Base with Docutray

## Endpoint

- **Method:** `GET`
- **Path:** `api/knowledge-bases/:id/search`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Search Knowledge Base](https://docs.docutray.com/docs/operations/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of the Knowledge Base |
| `includeMetadata` | query | `boolean` | no | Include metadata in results |
| `query` | query | `string` | yes | Search query |
| `similarityThreshold` | query | `number` | no | Minimum similarity threshold between 0 and 1 |
