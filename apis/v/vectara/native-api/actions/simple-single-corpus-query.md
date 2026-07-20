# Simple Single Corpus Query with Vectara

Retrieves query results from a specific Vectara corpus.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/corpora/:corpus_key/query`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Simple Single Corpus Query](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `query` | query | `string` | yes | Question or search text to run against the corpus. |
| `limit` | query | `number` | no | Maximum number of results to return. |
| `offset` | query | `number` | no | Number of results to skip. |
| `save_history` | query | `boolean` | no | Whether to save this query in history. |
| `intelligent_query_rewriting` | query | `boolean` | no | Enable query rewriting and filter extraction improvements. |
