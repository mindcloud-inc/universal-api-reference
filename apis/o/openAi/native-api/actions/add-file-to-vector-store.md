# Add File To Vector Store with Open AI

Adds a file to a vector store in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/vector_stores/:vector_store_id/files`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Add File To Vector Store](https://developers.openai.com/api/reference/resources/vector_stores/subresources/files/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vector_store_id` | path | `string` | yes | The ID of the vector store. |
| `file_id` | body | `string` | yes | The ID of the uploaded file to attach. |
