# Extract Document Field Values with Document AI

Extracts field values from a document using Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/fields`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Extract Document Field Values](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-fields-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file to extract named fields from. |
| `FieldNames` | body | `string` | yes | Comma-separated field names sent as the Cloudmersive FieldNames header. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
