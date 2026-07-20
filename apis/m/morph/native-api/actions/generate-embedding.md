# Generate Embedding with Morph

Generates embeddings with Morph.

## Endpoint

- **Method:** `POST`
- **Path:** `/embeddings`
- **Base URL:** `https://api.morphllm.com/v1`
- **Official documentation:** [Generate Embedding](https://docs.morphllm.com/api-reference/endpoint/embedding)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The code or text to generate embeddings for. |
| `encoding_format` | body | `string` | no | The format in which embeddings are returned. |
