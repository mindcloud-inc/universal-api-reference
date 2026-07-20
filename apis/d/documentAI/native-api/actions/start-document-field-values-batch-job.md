# Start Document Field Values Batch Job with Document AI

Creates a document field extraction batch job in Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/batch-job/extract/fields/advanced`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Start Document Field Values Batch Job](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-extract-fields-advanced-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `string` | yes | Base64-encoded document content for the batch field extraction job. |
| `FieldsToExtract[]` | body | `array<object>` | yes | Fields to extract from the document. |
| `recognitionMode` | body | `string` | no | Recognition mode sent as the Cloudmersive recognitionMode header. |
| `MaximumPagesProcessed` | body | `number` | no | Maximum number of pages to process. |
| `Preprocessing` | body | `string` | no | Optional preprocessing mode. |
| `ResultCrossCheck` | body | `string` | no | Optional result cross-check mode. |
| `RotateImageDegrees` | body | `number` | no | Optional image rotation in degrees. |
