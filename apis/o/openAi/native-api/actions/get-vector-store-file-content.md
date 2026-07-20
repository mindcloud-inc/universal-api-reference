# Get Vector Store File Content with Open AI

Retrieves vector store file contents from Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/vector_stores/:vector_store_id/files/:file_id/content`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Get Vector Store File Content](https://developers.openai.com/api/reference/vector-stores-files/retrieve-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | Vector store file ID whose parsed contents to retrieve. |
| `vector_store_id` | path | `string` | yes | Vector store ID that owns the file. |
