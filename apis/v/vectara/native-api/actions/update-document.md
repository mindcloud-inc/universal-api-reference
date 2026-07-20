# Update Document with Vectara

Updates an existing document in a specific Vectara corpus.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/corpora/:corpus_key/documents/:document_id`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Update Document](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `document_id` | path | `string` | yes | Unique ID of the document. |
| `metadata` | body | `object` | no | Document metadata fields to merge into the existing document metadata. |
