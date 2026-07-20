# Sync Knowledge Base with Docutray

## Endpoint

- **Method:** `POST`
- **Path:** `api/knowledge-bases/:id/sync`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [Sync Knowledge Base](https://docs.docutray.com/docs/operations/knowledge-bases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of the Knowledge Base |
| `force` | body | `boolean` | no | Force regeneration of all embeddings |
| `regenerateEmbeddings` | body | `boolean` | no | Regenerate existing embeddings |
| `syncExternalSources` | body | `boolean` | no | Sync with configured external sources |
