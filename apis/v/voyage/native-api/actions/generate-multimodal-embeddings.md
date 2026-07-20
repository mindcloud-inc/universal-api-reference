# Generate Multimodal Embeddings with Voyage

Generates multimodal embeddings in Voyage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/multimodalembeddings`
- **Base URL:** `https://api.voyageai.com`
- **Official documentation:** [Generate Multimodal Embeddings](https://docs.voyageai.com/reference/multimodal-embeddings-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inputs[]` | body | `array<object>` | yes | Multimodal inputs to embed. |
| `model` | body | `string` | yes | Multimodal embedding model to use. |
| `input_type` | body | `list` | no | Optional input type for retrieval-aware embeddings. Accepted values: `0`, `1`. |
