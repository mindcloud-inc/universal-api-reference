# Rerank Documents with Morph

Reranks documents with Morph.

## Endpoint

- **Method:** `POST`
- **Path:** `/rerank`
- **Base URL:** `https://api.morphllm.com/v1`
- **Official documentation:** [Rerank Documents](https://docs.morphllm.com/api-reference/endpoint/rerank)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Query to score each document against. |
| `documents[]` | body | `array<string>` | yes | Documents to rerank by relevance. |
| `top_n` | body | `number` | no | Optional number of top-ranked documents to return. |
