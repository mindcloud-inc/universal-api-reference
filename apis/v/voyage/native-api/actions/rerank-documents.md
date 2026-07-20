# Rerank Documents with Voyage

Reranks documents in Voyage for a query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/rerank`
- **Base URL:** `https://api.voyageai.com`
- **Official documentation:** [Rerank Documents](https://docs.voyageai.com/reference/reranker-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Query text used to rerank documents. |
| `documents[]` | body | `array<string>` | yes | Documents to rerank. |
| `model` | body | `string` | yes | Reranker model to use. |
| `top_k` | body | `number` | no | Maximum number of reranked documents to return. |
| `return_documents` | body | `boolean` | no | Whether to include documents in the response. |
