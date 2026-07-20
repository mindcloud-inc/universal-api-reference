# Rerank Results with Pinecone

Reranks search results with a Pinecone model.

## Endpoint

- **Method:** `POST`
- **Path:** `/rerank`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Rerank Results](https://docs.pinecone.io/reference/api/2025-10/inference/rerank)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | The reranking model to use. |
| `query` | body | `string` | yes | The query to rerank against. |
| `documents` | body | `list<object>` | yes | The list of document objects to rerank. Pass an array like [{"text":"..."},{"text":"..."}]. |
| `top_n` | body | `number` | no | Optional number of top results to return. |
