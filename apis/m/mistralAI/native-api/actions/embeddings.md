# Embeddings with Mistral AI

Creates text embeddings in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/embeddings`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Embeddings](https://docs.mistral.ai/api/endpoint/embeddings#operation-embeddings_v1_embeddings_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | ID of the model to use. |
| `input[]` | body | `array<string>` | yes | Text input strings to embed. |
| `output_dimension` | body | `number` | no | Requested embedding dimension when supported by the model. |
| `output_dtype` | body | `string` | no | Output numeric dtype for the embedding vector. |
| `encoding_format` | body | `string` | no | Encoding format for the embedding output. |
| `metadata` | body | `object` | no | Optional metadata object for the request. |
