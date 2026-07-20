# Create Embedding with Open AI

Creates text embeddings in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/embeddings`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Embedding](https://developers.openai.com/api/reference/resources/embeddings/methods/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `list` | yes | Embedding model ID. |
| `input` | body | `string` | yes | Input text or token array to embed. |
