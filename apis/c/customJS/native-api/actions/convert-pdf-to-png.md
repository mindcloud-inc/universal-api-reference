# Convert PDF to PNG with CustomJS

Converts a PDF to PNG images in CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/__js1-`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Convert PDF to PNG](https://www.customjs.space/integration/pdf-api/pdf-to-png/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.url` | body | `string` | yes | URL of the PDF file to convert. |
