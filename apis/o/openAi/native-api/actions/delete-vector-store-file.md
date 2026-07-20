# Delete Vector Store File with Open AI

Deletes a vector store file from Open AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1/vector_stores/:vector_store_id/files/:file_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Delete Vector Store File](https://developers.openai.com/api/reference/vector-stores-files/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | Vector store file ID to delete. |
| `vector_store_id` | path | `string` | yes | Vector store ID that owns the file. |
