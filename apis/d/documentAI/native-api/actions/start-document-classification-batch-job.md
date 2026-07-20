# Start Document Classification Batch Job with Document AI

Creates a document classification batch job in Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/batch-job/extract/classify`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Start Document Classification Batch Job](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-extract-classify-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file for the batch classification job. |
| `Categories` | body | `string` | yes | Comma-separated document categories sent as the Cloudmersive Categories header. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
