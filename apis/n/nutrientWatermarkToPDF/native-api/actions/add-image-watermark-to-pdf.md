# Add Image Watermark to PDF with Nutrient - Watermark to PDF

Updates a PDF with an image watermark in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Add Image Watermark to PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `file` | yes | PDF file to watermark. |
| `logo` | body | `file` | yes | Image file to use as the watermark. |
| `instructions` | body | `object` | yes | Build instructions for an image watermark. The image key must match the Logo Image field. |
