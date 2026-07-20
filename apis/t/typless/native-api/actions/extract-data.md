# Extract Data with Typless

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/extract-data`
- **Base URL:** `https://developers.typless.com`
- **Official documentation:** [Extract Data](https://typless.gitbook.io/typlessapi/methods/extract-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Original filename of the document being extracted. |
| `file` | body | `string` | yes | Base64-encoded file content to extract. |
| `document_type_name` | body | `string` | yes | Typless document type name to use for extraction. |
| `customer` | body | `string` | no | Optional customer identifier for the extraction. |
