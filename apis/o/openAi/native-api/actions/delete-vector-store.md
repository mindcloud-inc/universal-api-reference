# Delete Vector Store with Open AI

Deletes a vector store from Open AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1/vector_stores/:vector_store_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Delete Vector Store](https://developers.openai.com/api/reference/vector-stores/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vector_store_id` | path | `string` | yes | Vector store ID to delete. |
