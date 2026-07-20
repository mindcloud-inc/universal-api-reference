# Extract Text with OCR with api4ai

Extracts text from an image URL in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocr/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Extract Text with OCR](https://api4.ai/docs/ocr)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly reachable image URL to analyze. |
