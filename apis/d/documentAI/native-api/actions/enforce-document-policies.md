# Enforce Document Policies with Document AI

Evaluates a document against policies in Document AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-ai/document/analyze/enforce-policy`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Enforce Document Policies](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-analyze-enforce-policy-post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InputFile` | body | `string` | yes | Base64-encoded document content to check against policy rules. |
| `Rules[]` | body | `array<object>` | yes | Policy rules to evaluate against the document. |
| `RecognitionMode` | body | `string` | no | OCR recognition mode. |
