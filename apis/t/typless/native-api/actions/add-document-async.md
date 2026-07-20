# Add Document Async with Typless

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/add-document-async`
- **Base URL:** `https://developers.typless.com`
- **Official documentation:** [Add Document Async](https://typless.gitbook.io/typlessapi/methods/add-document-async)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Original filename of the dataset document being added asynchronously. |
| `file` | body | `string` | yes | Base64-encoded file content for the async dataset document. |
| `document_type_name` | body | `string` | yes | Typless document type name for the async dataset document. |
| `learning_fields` | body | `object` | yes | Ground-truth learning fields for the async dataset document. |
| `line_items` | body | `object` | no | Optional line item ground-truth values for the async dataset document. |
| `vat_rates` | body | `object` | no | Optional VAT rate ground-truth values for the async dataset document. |
