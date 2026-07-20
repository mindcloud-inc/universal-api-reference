# List Models with Pinecone

Retrieves available inference models from Pinecone.

## Endpoint

- **Method:** `GET`
- **Path:** `/models`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [List Models](https://docs.pinecone.io/reference/api/2025-10/inference/list_models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Optional model type filter: embed or rerank. |
| `vector_type` | query | `string` | no | Optional embedding vector type filter: dense or sparse. |
