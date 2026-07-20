# Add Text Watermark to PDF with Nutrient - Watermark to PDF

Updates a PDF with a text watermark in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Add Text Watermark to PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `file` | yes | PDF file to watermark. |
| `instructions` | body | `object` | yes | Build instructions for a text watermark. Edit the text, position, color, opacity, or dimensions as needed. |
