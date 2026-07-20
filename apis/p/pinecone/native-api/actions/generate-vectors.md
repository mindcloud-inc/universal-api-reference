# Generate Vectors with Pinecone

Generates vectors from input data in Pinecone.

## Endpoint

- **Method:** `POST`
- **Path:** `/embed`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Generate Vectors](https://docs.pinecone.io/reference/api/2025-10/inference/generate-embeddings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | The embedding model to use. |
| `inputs[].text` | body | `string` | yes | The text input to generate an embedding for. |
| `parameters.input_type` | body | `string` | yes | The input type required by the model: query or passage. |
| `parameters.truncate` | body | `string` | no | Optional truncation behavior for overlong inputs. |
