# Convert Remote PDF to Image with Nutrient Document Converter

Converts a remote PDF to images in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Convert Remote PDF to Image](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-to-image-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdfUrl` | body | `string` | yes | Publicly reachable PDF URL. |
| `format` | body | `string` | no | Image format to output. |
| `pageStart` | body | `number` | no | Zero-based first page to render. |
| `pageEnd` | body | `number` | no | Zero-based last page to render; use -1 for all pages. |
| `width` | body | `number` | no | Optional output width in pixels. |
