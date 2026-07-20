# List Documents with PDFMonkey

Retrieves documents from PDFMonkey.

## Endpoint

- **Method:** `GET`
- **Path:** `/document_cards`
- **Base URL:** `https://api.pdfmonkey.io/api/v1`
- **Official documentation:** [List Documents](https://pdfmonkey.io/docs/api/documents/#list-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page[number]` | query | `number` | no | Results page number. |
| `q[document_template_id]` | query | `string` | no | Template IDs to filter on. Send multiple values as a array. |
| `q[status]` | query | `string` | no | Document status to filter on. |
| `q[workspace_id]` | query | `string` | no | Workspace ID to filter on. |
| `q[updated_since]` | query | `number` | no | Unix timestamp filter for recently updated documents. |
