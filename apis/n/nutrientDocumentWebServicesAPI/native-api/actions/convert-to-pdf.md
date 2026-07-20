# Convert to PDF with Nutrient Document Web Services

Creates a PDF document in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/convert_to_pdf`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert to PDF](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-convert-to-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Public file URL to convert. |
| `file` | body | `file` | no | File to upload for conversion. |
| `password` | body | `string` | no | Password for protected source files. |
| `layout` | body | `object` | no | Layout settings for the generated PDF. |
| `pages` | body | `object` | no | Page range to include. |
| `content_type` | body | `string` | no | MIME type of the source file URL. |
| `markup_mode` | body | `string` | no | Markup conversion mode. |
| `data` | body | `object` | no | Multipart request metadata. |
