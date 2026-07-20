# Get Vector Store File with Open AI

Retrieves a vector store file from Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/vector_stores/:vector_store_id/files/:file_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Get Vector Store File](https://developers.openai.com/api/reference/vector-stores-files/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | Vector store file ID to retrieve. |
| `vector_store_id` | path | `string` | yes | Vector store ID that owns the file. |
