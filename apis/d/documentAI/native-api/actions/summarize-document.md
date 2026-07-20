# Summarize Document with Document AI

Generates a one-paragraph summary of a document using Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/summary`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Summarize Document](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-summary-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file to summarize. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
| `language` | body | `string` | no | Optional three-letter ISO 639 language code sent as a request header. |
