# Upload Document For Capturing with Natif.ai

Creates a new document for capturing in Natif.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [Upload Document For Capturing](https://api.natif.ai/docs#/Document%20Capturing/upload_document_documents_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document file to upload. Supported file types include jpg, jpeg, tif, tiff, png, pdf, gif, and webp. |
| `document_type` | query | `string` | no | Document type. Natif.ai determines the type automatically when omitted. |
| `language` | query | `string` | no | Document language. Defaults to `de`; use `xx` when unknown. |
| `generate_pdf` | query | `list` | no | Generate a downloadable PDF from processed pages. Accepted values: `OCR Text Layer`, `ZUGFeRD`. |
| `process_definition_key` | query | `string` | no | Workflow key to use for processing. |
| `preview` | query | `boolean` | no | Run the upload in preview mode. |
