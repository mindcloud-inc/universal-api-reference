# Add Page Range Watermark to PDF with Nutrient - Watermark to PDF

Updates selected PDF pages with a watermark in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Add Page Range Watermark to PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `file` | yes | PDF file to watermark. |
| `instructions` | body | `object` | yes | Build instructions with a page selection. Adjust pages.start and pages.end to choose the target range. |
