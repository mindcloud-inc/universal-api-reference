# Extract PDF To Structured Data with PDF-app

Retrieves structured data from a PDF in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/conv_classification`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Extract PDF To Structured Data](https://pdf-app.net/apidocumentation?type=conv_classification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | PDF URL to convert and analyze. |
| `doClassification` | body | `boolean` | no | Whether to classify entities in the extracted text. |
| `doSensitivity` | body | `boolean` | no | Whether to detect PII in the extracted text. |
| `onlyTables` | body | `boolean` | no | Whether to include only table data in the output file. |
| `ocrPages[]` | body | `array<number>` | no | 1-based page numbers that should be forced through OCR. |
| `include_pii_values` | body | `boolean` | no | Whether to return the actual PII values in detection results. |
| `exclude_file_return` | body | `boolean` | no | Whether to skip generation of a downloadable output file. |
| `format` | body | `string` | no | Desired output format: excel, csv, text, or none. |
| `language` | body | `string` | no | OCR language code used during processing. |
| `async` | body | `boolean` | no | Whether to run the conversion asynchronously. |
