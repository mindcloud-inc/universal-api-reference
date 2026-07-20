# Split PDF by page with Aquaforest PDF

Splits PDF files by page range in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/SplitPdfByPage`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Split PDF by page](https://learn.microsoft.com/en-us/connectors/aquaforest/#split-pdf-by-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the source PDF file. |
| `sourceFileName` | body | `string` | yes | The name of the source file. |
| `fileNameTemplate` | body | `string` | yes | Template for each output file name. |
| `splitOption` | body | `string` | no | How the PDF should be split into output files. |
| `pageRange` | body | `string` | no | Page range to split, for example 1 or 1-3. |
