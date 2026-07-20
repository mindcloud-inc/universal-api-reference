# Retrieve Relevant Chunks with Graphor

Retrieves relevant document chunks from Graphor by semantic search.

## Endpoint

- **Method:** `POST`
- **Path:** `/prebuilt-rag`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Retrieve Relevant Chunks](https://docs.graphorlm.com/api-reference/prebuilt-rag-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids` | body | `string` | no | Optional list of file IDs to scope retrieval to specific documents. |
| `query` | body | `string` | yes | The semantic-search query used to retrieve relevant chunks. |
