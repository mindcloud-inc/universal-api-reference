# Extract PDF pages by barcode with Aquaforest PDF

Extracts PDF pages by barcode matches in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/ExtractPageByBarcode`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Extract PDF pages by barcode](https://learn.microsoft.com/en-us/connectors/aquaforest/#extract-pdf-pages-by-barcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the source PDF file. |
| `sourceFileName` | body | `string` | yes | The name of the source file. |
| `fileNameTemplate` | body | `string` | yes | Template for the output file if barcode is found. |
| `noTextFileName` | body | `string` | yes | Template for the output file if no barcode is found. |
| `zones[]` | body | `array<object>` | no | Barcode extraction zone objects with location, barcodeFormats, and optional regex. |
