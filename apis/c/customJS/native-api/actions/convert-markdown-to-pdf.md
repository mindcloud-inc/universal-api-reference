# Convert Markdown to PDF with CustomJS

Converts Markdown to a PDF in CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/markdown2pdf`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Convert Markdown to PDF](https://www.customjs.space/integration/native-api/documentation/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.markdown` | body | `string` | yes | Markdown content to convert to PDF. |
