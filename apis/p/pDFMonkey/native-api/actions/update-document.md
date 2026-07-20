# Update Document with PDFMonkey

Updates an existing document in PDFMonkey.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:id`
- **Base URL:** `https://api.pdfmonkey.io/api/v1`
- **Official documentation:** [Update Document](https://pdfmonkey.io/docs/api/documents/#update-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the Document to update. |
| `document.document_template_id` | body | `string` | no | ID of the source Template to use. |
| `document.status` | body | `string` | no | Document lifecycle state. Use pending to queue generation immediately. |
| `document.payload` | body | `object` | no | Data used for document generation. |
| `document.meta` | body | `object` | no | Meta-data to attach to the document. |
