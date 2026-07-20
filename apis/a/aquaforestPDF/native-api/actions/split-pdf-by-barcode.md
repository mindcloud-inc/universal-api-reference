# Split PDF by barcode with Aquaforest PDF

Splits PDF files by barcode matches in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/SplitByBarcode`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Split PDF by barcode](https://learn.microsoft.com/en-us/connectors/aquaforest/#split-pdf-by-barcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the source PDF file. |
| `sourceFileName` | body | `string` | yes | The name of the source file. |
| `fileNameTemplate` | body | `string` | yes | Template for the output file if a barcode is found. |
| `noTextFileName` | body | `string` | yes | Template for the output file if no barcode is found. |
| `splitOption` | body | `string` | no | How pages are grouped around matched barcode pages. |
| `noMatch` | body | `string` | no | What to do with pages that have no barcode value. |
| `zones[]` | body | `array<object>` | no | Barcode matching zone objects with location, barcodeFormats, and optional regex. |
