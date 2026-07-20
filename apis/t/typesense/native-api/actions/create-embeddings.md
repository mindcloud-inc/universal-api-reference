# Create Embeddings with Typesense

Creates new vector embeddings in Typesense.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/embeddings`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Create Embeddings](https://typesense.org/docs/30.0/api/vector-search.html#generating-embeddings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `embeddingRequest` | body | `object` | yes | OpenAI-compatible embedding request body. |
