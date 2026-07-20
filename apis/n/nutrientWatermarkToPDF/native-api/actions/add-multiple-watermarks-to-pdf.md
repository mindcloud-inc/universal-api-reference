# Add Multiple Watermarks to PDF with Nutrient - Watermark to PDF

Updates a PDF with multiple watermarks in Nutrient.

## Endpoint

- **Method:** `POST`
- **Path:** `/build`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Add Multiple Watermarks to PDF](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `file` | yes | PDF file to watermark. |
| `logo` | body | `file` | yes | Image file to use as one of the watermarks. |
| `instructions` | body | `object` | yes | Build instructions for applying multiple watermarks in one request. |
