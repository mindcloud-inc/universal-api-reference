# List Documents with Vectara

Retrieves documents from a specific Vectara corpus.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/corpora/:corpus_key/documents`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [List Documents](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `limit` | query | `number` | no | Maximum number of documents to return. |
| `metadata_filter` | query | `string` | no | Metadata filter expression used to narrow listed documents. |
| `page_key` | query | `string` | no | Cursor for the next page of documents. |
