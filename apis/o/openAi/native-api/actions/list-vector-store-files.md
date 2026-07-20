# List Vector Store Files with Open AI

Retrieves vector store files from Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/vector_stores/:vector_store_id/files`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [List Vector Store Files](https://developers.openai.com/api/reference/vector-stores-files/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vector_store_id` | path | `string` | yes | Vector store ID whose files to list. |
