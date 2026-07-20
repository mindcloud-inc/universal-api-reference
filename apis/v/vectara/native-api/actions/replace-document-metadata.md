# Replace Document Metadata with Vectara

Replaces metadata for a document in a Vectara corpus.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/corpora/:corpus_key/documents/:document_id/metadata`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Replace Document Metadata](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `document_id` | path | `string` | yes | Unique ID of the document. |
| `metadata` | body | `object` | no | Document metadata object that replaces the existing metadata. |
