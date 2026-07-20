# Advanced Single Corpus Query with Vectara

Retrieves advanced query results from a specific Vectara corpus.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/corpora/:corpus_key/query`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Advanced Single Corpus Query](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `query` | body | `string` | yes | Question or search text to run against the corpus. |
| `search.metadata_filter` | body | `string` | no | Metadata filter expression for corpus search results. |
| `search.lexical_interpolation` | body | `number` | no | Blend factor between semantic and lexical retrieval. |
| `search.limit` | body | `number` | no | Maximum number of results to retrieve before reranking. |
| `search.offset` | body | `number` | no | Number of search results to skip. |
| `search.context_configuration` | body | `object` | no | Context window configuration for each search result. |
| `search.reranker` | body | `object` | no | Reranker configuration object. |
| `generation.generation_preset_name` | body | `string` | no | Generation preset to use for grounded generation. |
| `generation.prompt_template` | body | `string` | no | Optional custom prompt template for generation. |
| `generation.max_used_search_results` | body | `number` | no | Maximum number of top search results sent to generation. |
| `generation.response_language` | body | `string` | no | Language code for the generated response. |
| `generation.model_parameters` | body | `object` | no | Optional model parameter overrides for generation. |
| `generation.citations` | body | `object` | no | Citation formatting configuration. |
| `generation.enable_factual_consistency_score` | body | `boolean` | no | Whether to include a factual consistency score. |
| `stream_response` | body | `boolean` | no | Whether to stream the query response. |
| `save_history` | body | `boolean` | no | Whether to save this query in history. |
| `intelligent_query_rewriting` | body | `boolean` | no | Enable query rewriting and metadata filter extraction. |
