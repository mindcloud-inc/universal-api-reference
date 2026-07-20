# Classify Document Advanced with Document AI

Classifies a document using advanced Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/classify/advanced`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Classify Document Advanced](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-classify-advanced-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `string` | yes | Base64-encoded document content to classify. |
| `Categories[]` | body | `array<object>` | yes | Document classification categories to evaluate. |
| `recognitionMode` | body | `string` | no | Recognition mode sent as the Cloudmersive recognitionMode header. |
| `Preprocessing` | body | `string` | no | Optional preprocessing mode for document classification. |
| `ResultCrossCheck` | body | `string` | no | Optional result cross-check mode. |
| `MaximumPagesProcessed` | body | `number` | no | Maximum number of pages to process. |
| `RotateImageDegrees` | body | `number` | no | Optional image rotation in degrees before classification. |
