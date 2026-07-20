# Convert PDF to Text with CustomJS

Extracts text from a PDF in CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/__js1-`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Convert PDF to Text](https://www.customjs.space/integration/pdf-api/pdf-to-text/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.url` | body | `string` | yes | URL of the PDF file to convert to text. |
