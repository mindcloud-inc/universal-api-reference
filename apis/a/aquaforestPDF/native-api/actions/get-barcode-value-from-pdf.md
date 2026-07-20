# Get barcode value from PDF with Aquaforest PDF

Retrieves barcode values from PDFs in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/GetBarcodeValue`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Get barcode value from PDF](https://learn.microsoft.com/en-us/connectors/aquaforest/#get-barcode-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the source PDF file. |
| `sourceFileName` | body | `string` | yes | The name of the source file. |
| `barcodeResultTemplate` | body | `string` | yes | Template for the output text result if a barcode is found. |
| `noBarcodeTemplate` | body | `string` | yes | Template for the output text result if no barcode is found. |
| `pagerange` | body | `string` | no | Page range to inspect, such as 1,2,4-7. |
| `zones[]` | body | `array<object>` | no | Barcode extraction zone objects with location, barcodeFormats, pagenumber, and optional regex. |
