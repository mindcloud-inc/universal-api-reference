# Create Landscape Webpage PDF with DocMaker

Creates a landscape webpage PDF in DocMaker.

## Endpoint

- **Method:** `POST`
- **Path:** `/page_pdf`
- **Base URL:** `https://api.v2.docmaker.co`
- **Official documentation:** [Create Landscape Webpage PDF](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `url` | body | `string` | yes |
| `metadata` | body | `string` | no |
