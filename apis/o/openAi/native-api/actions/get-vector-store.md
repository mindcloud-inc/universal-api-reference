# Get Vector Store with Open AI

Retrieves a vector store from Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/vector_stores/:vector_store_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Get Vector Store](https://developers.openai.com/api/reference/vector-stores/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vector_store_id` | path | `string` | yes | Vector store ID to retrieve. |
