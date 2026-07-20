# Search Vector Store with Open AI

Searches a vector store in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/vector_stores/:vector_store_id/search`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Search Vector Store](https://developers.openai.com/api/reference/resources/vector_stores/methods/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vector_store_id` | path | `string` | yes | The ID of the vector store to search. |
| `query` | body | `string` | yes | Natural language query used for semantic search. |
