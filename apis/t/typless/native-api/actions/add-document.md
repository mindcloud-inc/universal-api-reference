# Add Document with Typless

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/add-document`
- **Base URL:** `https://developers.typless.com`
- **Official documentation:** [Add Document](https://typless.gitbook.io/typlessapi/methods/add-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `learning_fields` | body | `object` | yes | Ground-truth learning fields for the document being added to the dataset. |
| `file_name` | body | `string` | yes | Original filename of the document being added to the dataset. |
| `file` | body | `string` | yes | Base64-encoded file content for the dataset document. |
| `document_type_name` | body | `string` | no | Optional Typless document type name for the dataset document. |
| `line_items` | body | `object` | no | Optional line item ground-truth values for the dataset document. |
| `vat_rates` | body | `object` | no | Optional VAT rate ground-truth values for the dataset document. |
