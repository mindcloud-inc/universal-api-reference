# Generate Document Synchronously with PDFMonkey

Generates a document synchronously in PDFMonkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/sync`
- **Base URL:** `https://api.pdfmonkey.io/api/v1`
- **Official documentation:** [Generate Document Synchronously](https://pdfmonkey.io/docs/api/documents/#synchronous-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document.document_template_id` | body | `string` | yes | ID of the source Template to use. |
| `document.payload` | body | `object` | no | Data to use for the Document generation. |
| `document.meta` | body | `object` | no | Meta-data to attach to the Document. |
