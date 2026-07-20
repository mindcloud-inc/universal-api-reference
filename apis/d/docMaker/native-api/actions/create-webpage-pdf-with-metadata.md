# Create Webpage PDF With Metadata with DocMaker

Creates a webpage PDF with metadata in DocMaker.

## Endpoint

- **Method:** `POST`
- **Path:** `/page_pdf`
- **Base URL:** `https://api.v2.docmaker.co`
- **Official documentation:** [Create Webpage PDF With Metadata](https://guide.docmaker.co/features/print-web-page-to-pdf/page_pdf-api-parameters)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `url` | body | `string` | yes |
| `pageSize` | body | `string` | yes |
| `landscape` | body | `boolean` | yes |
| `metadata` | body | `string` | yes |
