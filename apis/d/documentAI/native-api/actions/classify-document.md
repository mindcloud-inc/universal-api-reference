# Classify Document with Document AI

Classifies a document using Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/classify`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Classify Document](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-classify-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file to classify. |
| `Categories` | body | `string` | yes | Comma-separated document categories sent as the Cloudmersive Categories header. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
