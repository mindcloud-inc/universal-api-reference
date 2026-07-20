# Start Document Fields and Tables Batch Job with Document AI

Creates a document extraction batch job in Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/batch-job/extract/all`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Start Document Fields and Tables Batch Job](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-extract-all-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file for the batch fields and tables extraction job. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
