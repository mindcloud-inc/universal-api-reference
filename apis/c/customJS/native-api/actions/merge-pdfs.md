# Merge PDFs with CustomJS

Merges PDF files into one PDF in CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/__js1-`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Merge PDFs](https://www.customjs.space/integration/pdf-api/merge-pdfs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.urls[]` | body | `array<string>` | yes | List of PDF URLs to merge in order. |
