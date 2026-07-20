# Query Metadata with Vectara

Queries metadata fields in a specific Vectara corpus.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/corpora/:corpus_key/metadata_query`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Query Metadata](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `queries[]` | body | `array<object>` | yes | Array of field-specific metadata queries to match. |
| `level` | body | `list` | no | Whether to search document-level or part-level metadata. Accepted values: `0`, `1`. |
| `metadata_filter` | body | `string` | no | Exact metadata filter applied before fuzzy matching. |
| `limit` | body | `number` | no | Maximum number of matched documents to return. |
| `offset` | body | `number` | no | Number of matching results to skip. |
