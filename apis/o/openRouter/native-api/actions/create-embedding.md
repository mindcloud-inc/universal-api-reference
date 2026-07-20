# Create Embedding with OpenRouter

Creates a new embedding in OpenRouter.

## Endpoint

- **Method:** `POST`
- **Path:** `/embeddings`
- **Base URL:** `https://openrouter.ai/api/v1/`
- **Official documentation:** [Create Embedding](https://openrouter.ai/docs/api/api-reference/embeddings/create-embeddings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Input text to embed. |
| `model` | body | `string` | yes | Embedding model identifier. |
