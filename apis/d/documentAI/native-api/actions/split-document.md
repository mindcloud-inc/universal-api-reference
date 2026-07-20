# Split Document with Document AI

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/split`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Split Document](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-split-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `file` | yes | Document file to split. |
| `recognitionMode` | body | `string` | no | Optional recognition mode sent as a request header. |
