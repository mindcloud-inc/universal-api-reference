# Convert HTML to PDF with Nutrient Document Web Services

Creates a PDF document from HTML in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/generate_pdf`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert HTML to PDF](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-generate-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Web page URL to render as PDF. |
| `html` | body | `string` | no | Raw HTML to render as PDF. |
| `assets[]` | body | `array<string>` | no | Referenced assets for HTML rendering. |
| `layout` | body | `object` | no | PDF page layout settings. |
| `data` | body | `object` | no | Multipart request metadata. |
