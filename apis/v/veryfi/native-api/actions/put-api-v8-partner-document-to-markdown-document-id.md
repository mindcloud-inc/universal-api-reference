# Update a Markdown Document with Veryfi

Updates an existing markdown document in Veryfi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v8/partner/document-to-markdown/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Update a Markdown Document](https://docs.veryfi.com/api/document-to-markdown/update-a-markdown-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `status` | body | `string` | no | Update the document status |
