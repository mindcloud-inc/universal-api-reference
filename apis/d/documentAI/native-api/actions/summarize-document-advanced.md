# Summarize Document Advanced with Document AI

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/extract/summary/advanced`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Summarize Document Advanced](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-summary-advanced-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `string` | yes | Base64-encoded document content to summarize. |
| `RecognitionMode` | body | `string` | no | OCR recognition mode. |
| `Language` | body | `string` | no | Language code for summarization. |
| `SummaryParagraphCount` | body | `number` | no | Number of paragraphs to include in the summary. |
