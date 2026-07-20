# Extract Document Tables with Document AI

Extracts tables from a document using Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/tables`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Extract Document Tables](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-tables-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file to extract tables from. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
