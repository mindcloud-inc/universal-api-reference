# Extract Document Barcodes with Document AI

Extracts barcodes from a document using Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/barcodes`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Extract Document Barcodes](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-barcodes-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file to extract barcodes from. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
