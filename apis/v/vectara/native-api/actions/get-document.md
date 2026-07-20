# Get Document with Vectara

Retrieves a document from a specific Vectara corpus.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/corpora/:corpus_key/documents/:document_id`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Get Document](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `document_id` | path | `string` | yes | Unique ID of the document. |
