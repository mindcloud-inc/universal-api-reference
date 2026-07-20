# Retrieve Relevant Chunks By File Name with Graphor

Retrieves relevant document chunks from Graphor by file name.

## Endpoint

- **Method:** `POST`
- **Path:** `/prebuilt-rag`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Retrieve Relevant Chunks By File Name](https://docs.graphorlm.com/api-reference/prebuilt-rag-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_names` | body | `string` | yes | Deprecated list of file names to scope retrieval to specific documents. |
| `query` | body | `string` | yes | The semantic-search query used to retrieve relevant chunks. |
