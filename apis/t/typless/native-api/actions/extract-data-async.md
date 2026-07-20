# Extract Data Async with Typless

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/extract-data-async`
- **Base URL:** `https://developers.typless.com`
- **Official documentation:** [Extract Data Async](https://typless.gitbook.io/typlessapi/methods/extract-data-async)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Original filename of the document being extracted asynchronously. |
| `file` | body | `string` | yes | Base64-encoded file content to extract asynchronously. |
| `document_type_name` | body | `string` | yes | Typless document type name to use for asynchronous extraction. |
| `parse_text_blocks` | body | `boolean` | no | Whether Typless should parse text blocks during async extraction. |
| `customer` | body | `string` | no | Optional customer identifier for the async extraction. |
