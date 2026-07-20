# Extract Text with OCR from File with api4ai

Extracts text from an image file in api4ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocr/v1/results`
- **Base URL:** `https://api4ai.cloud`
- **Official documentation:** [Extract Text with OCR from File](https://api4.ai/docs/ocr)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to analyze. |
