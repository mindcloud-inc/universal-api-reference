# Add Last Page Watermark to PDF with Nutrient - Watermark to PDF

Updates the last PDF page with a watermark in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Add Last Page Watermark to PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `file` | yes | PDF file to watermark. |
| `logo` | body | `file` | yes | Image file to apply on the last page. |
| `instructions` | body | `object` | yes | Build instructions that leave earlier pages unchanged and apply an image watermark to only the last page. |
