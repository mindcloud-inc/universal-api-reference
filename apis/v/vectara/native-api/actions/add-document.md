# Add Document with Vectara

Adds a document to a Vectara corpus for indexing.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/corpora/:corpus_key/documents`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Add Document](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `wait_for` | query | `list` | no | Wait until the document is searchable or fully indexed before returning. Accepted values: `0`, `1`. |
| `type` | body | `list` | yes | Document payload type. Accepted values: `0`, `1`. |
| `id` | body | `string` | yes | Unique document ID within the corpus. |
| `title` | body | `string` | no | Document title for structured documents. |
| `description` | body | `string` | no | Document description for structured documents. |
| `metadata` | body | `object` | no | Document-level metadata object. |
| `sections[]` | body | `array<object>` | no | Structured document sections array. |
| `document_parts[]` | body | `array<object>` | no | Core document parts array. |
| `custom_dimensions` | body | `object` | no | Document-level custom dimensions. |
| `chunking_strategy` | body | `object` | no | Optional chunking strategy for structured documents. |
