# Create Document with PDFMonkey

Creates a document asynchronously in PDFMonkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.pdfmonkey.io/api/v1`
- **Official documentation:** [Create Document](https://pdfmonkey.io/docs/api/documents/#create-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document.document_template_id` | body | `string` | yes | ID of the source Template to use. |
| `document.status` | body | `string` | no | Document lifecycle state. Use pending to queue generation immediately. |
| `document.payload` | body | `object` | no | Data used for document generation. |
| `document.meta` | body | `object` | no | Meta-data to attach to the document. |
