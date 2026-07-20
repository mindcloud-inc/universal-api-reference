# List Templates with PDFMonkey

Retrieves templates from PDFMonkey.

## Endpoint

- **Method:** `GET`
- **Path:** `/document_template_cards`
- **Base URL:** `https://api.pdfmonkey.io/api/v1`
- **Official documentation:** [List Templates](https://pdfmonkey.io/docs/api/templates/#list-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q[workspaceId]` | query | `string` | yes | Workspace to search within. |
| `q[folders]` | query | `string` | no | Comma-separated folder IDs to search within, or none for the root folder. |
| `page` | query | `number` | no | Page number to return. |
| `sort` | query | `string` | no | Attribute to sort by: identifier, created_at, or updated_at. |
