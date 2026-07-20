# Extract Pages from PDF with CustomJS

Extracts selected pages from a PDF in CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/__js1-`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Extract Pages from PDF](https://www.customjs.space/integration/pdf-api/extract-pages-from-pdf/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.pageRange` | body | `string` | yes | Page range to extract, for example 1-3. |
| `input.url` | body | `string` | yes | URL of the PDF file to extract pages from. |
