# Add Document Feedback with Typless

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/add-document-feedback`
- **Base URL:** `https://developers.typless.com`
- **Official documentation:** [Add Document Feedback](https://typless.gitbook.io/typlessapi/methods/add-document-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_type_name` | body | `string` | yes | Typless document type name for the document feedback. |
| `learning_fields` | body | `object` | yes | Corrected learning fields for the reviewed document. |
| `document_object_id` | body | `string` | yes | Typless dataset document object identifier. |
| `line_items` | body | `object` | no | Optional corrected line item values for the reviewed document. |
| `vat_rates` | body | `object` | no | Optional corrected VAT rate values for the reviewed document. |
