# Extract Document Text with Document AI

Extracts text from a document using Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/text`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Extract Document Text](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-text-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file to extract text from. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
