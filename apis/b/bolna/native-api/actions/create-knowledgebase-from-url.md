# Create Knowledgebase from URL with Bolna

Creates a new knowledgebase in Bolna from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/knowledgebase`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [Create Knowledgebase from URL](https://www.bolna.ai/docs/api-reference/knowledgebase/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL to ingest into the knowledgebase. |
| `chunk_size` | body | `number` | no | Chunk size for embedding model. |
| `similarity_top_k` | body | `number` | no | Number of top similar nodes to return. |
| `overlapping` | body | `number` | no | Overlap between neighboring nodes. |
| `language_support` | body | `string` | no | Enable multilingual retrieval mode. Accepted values: `0`. |
