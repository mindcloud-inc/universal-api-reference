# Create Contextualized Embeddings with Perplexity

Creates contextualized embeddings from text in Perplexity.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contextualizedembeddings`
- **Base URL:** `https://api.perplexity.ai`
- **Official documentation:** [Create Contextualized Embeddings](https://docs.perplexity.ai/api-reference/contextualized-embeddings-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<array>` | yes | Nested array of document chunks. Each inner array represents one document. |
| `model` | body | `string` | yes | Contextualized embedding model to use. |
| `dimensions` | body | `number` | no | Optional output embedding dimensions. |
