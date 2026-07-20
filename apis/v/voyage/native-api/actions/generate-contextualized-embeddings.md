# Generate Contextualized Embeddings with Voyage

Generates contextualized chunk embeddings in Voyage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contextualizedembeddings`
- **Base URL:** `https://api.voyageai.com`
- **Official documentation:** [Generate Contextualized Embeddings](https://docs.voyageai.com/reference/contextualized-embeddings-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs[]` | body | `array<array>` | yes | Nested input lists to embed with context. |
| `model` | body | `string` | yes | Contextualized embedding model to use. |
| `input_type` | body | `list` | no | Optional input type for retrieval-aware embeddings. Accepted values: `0`, `1`. |
