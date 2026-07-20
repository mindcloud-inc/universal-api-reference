# Upload File with Vectara

Uploads a file to a Vectara corpus for indexing.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/corpora/:corpus_key/upload_file`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Upload File](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `corpus_key` | path | `string` | yes | Unique key of the corpus. |
| `metadata` | body | `object` | no | Metadata object to attach to the uploaded document. |
| `chunking_strategy` | body | `object` | no | Chunking strategy for extracted text. |
| `table_extraction_config` | body | `object` | no | Table extraction configuration for supported files. |
| `filename` | body | `string` | no | Optional override for the uploaded filename or document ID. |
| `file` | body | `file` | yes | Binary file to upload. |
