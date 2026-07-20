# Create Embeddings with Perplexity

Creates embeddings from text in Perplexity.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/embeddings`
- **Base URL:** `https://api.perplexity.ai`
- **Official documentation:** [Create Embeddings](https://docs.perplexity.ai/api-reference/embeddings-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Input text to embed. Perplexity also accepts arrays of strings; this action currently models the common single-input path. |
| `model` | body | `string` | yes | Embedding model to use. |
| `dimensions` | body | `number` | no | Optional output embedding dimensions. |
| `encoding_format` | body | `string` | no | Output encoding format, for example base64_int8 or base64_binary. |
