# Create Webpage PDF With Custom Viewport with DocMaker

Creates a webpage PDF with custom viewport in DocMaker.

## Endpoint

- **Method:** `POST`
- **Path:** `/page_pdf`
- **Base URL:** `https://api.v2.docmaker.co`
- **Official documentation:** [Create Webpage PDF With Custom Viewport](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `url` | body | `string` | yes |
| `vWidth` | body | `number` | yes |
| `vHeight` | body | `number` | yes |
| `metadata` | body | `string` | no |
