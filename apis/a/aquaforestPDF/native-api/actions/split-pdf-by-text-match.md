# Split PDF by text match with Aquaforest PDF

Splits PDF files by text matches in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/SplitByText`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Split PDF by text match](https://learn.microsoft.com/en-us/connectors/aquaforest/#split-pdf-by-text-match)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the source PDF file. |
| `sourceFileName` | body | `string` | yes | The name of the source file. |
| `fileNameTemplate` | body | `string` | yes | Template for the output file if text matches are found. |
| `noTextFileName` | body | `string` | yes | Template for the output file if no text match is found. |
| `splitOption` | body | `string` | no | How pages are grouped around matched text pages. |
| `noMatch` | body | `string` | no | What to do with pages that have no text match. |
| `zones[]` | body | `array<object>` | no | Text matching zone objects with location, expression, position, and optional regex. |
