# Convert HTML to PDF with CustomJS

Converts HTML to a PDF in CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/html2pdf`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Convert HTML to PDF](https://www.customjs.space/integration/pdf-api/html-to-pdf/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.html` | body | `string` | yes | HTML content to convert to PDF. |
