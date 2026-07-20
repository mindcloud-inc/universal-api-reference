# Convert Markdown to PDF with Nutrient - Convert to PDF

Creates a PDF document from Markdown in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/md_to_pdf`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert Markdown to PDF](https://www.nutrient.io/api/md-to-pdf-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `markdown` | body | `string` | yes | Markdown content to render as a PDF. |
| `template` | body | `string` | no | Built-in or custom Markdown PDF template identifier. |
