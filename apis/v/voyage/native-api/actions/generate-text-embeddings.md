# Generate Text Embeddings with Voyage

Generates text vector embeddings in Voyage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/embeddings`
- **Base URL:** `https://api.voyageai.com`
- **Official documentation:** [Generate Text Embeddings](https://docs.voyageai.com/reference/embeddings-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<string>` | yes | Text input or list of text inputs to embed. |
| `model` | body | `string` | yes | Embedding model to use. |
| `input_type` | body | `list` | no | Optional input type for retrieval-aware embeddings. Accepted values: `0`, `1`. |
