# Extract Document Fields and Tables with Document AI

Extracts fields and tables from a document using Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/all`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Extract Document Fields and Tables](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-all-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file to extract fields and tables from. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
| `preprocessing` | body | `string` | no | Optional preprocessing level sent as a request header. |
