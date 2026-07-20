# Update Vector Store with Open AI

Updates a vector store in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/vector_stores/:vector_store_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Update Vector Store](https://developers.openai.com/api/reference/vector-stores/modify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Updated vector store name. |
| `vector_store_id` | path | `string` | yes | Vector store ID to update. |
