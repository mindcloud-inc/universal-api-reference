# Get Document with Libraria

Get a document from a library.

## Endpoint

- **Method:** `GET`
- **Path:** `/library/:library_id/document/:document_id`
- **Base URL:** `https://api.libraria.ai`
- **Official documentation:** [Get Document](https://docs.libraria.ai/api-reference/library/get-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `library_id` | path | `string` | yes | The ID of the library that owns the document. |
| `document_id` | path | `string` | yes | The ID of the document to retrieve. |
