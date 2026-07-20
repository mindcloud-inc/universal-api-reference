# PDF/UA Auto-Tagging with Nutrient Document Web Services

Creates a PDF/UA document in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/processor/pdfua`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [PDF/UA Auto-Tagging](https://www.nutrient.io/api/reference/public/#tag/Document-Editing/operation/processor-pdfua)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Public PDF URL to convert to PDF/UA. |
| `file` | body | `file` | no | PDF file to convert to PDF/UA. |
| `password` | body | `string` | no | Password for protected PDF files. |
| `data` | body | `object` | no | Multipart request metadata. |
