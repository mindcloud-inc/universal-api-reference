# Extract PDF pages by text with Aquaforest PDF

Extracts PDF pages by text matches in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/ExtractPageByText`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Extract PDF pages by text](https://learn.microsoft.com/en-us/connectors/aquaforest/#extract-pdf-pages-by-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the source PDF file. |
| `sourceFileName` | body | `string` | yes | The name of the source file. |
| `fileNameTemplate` | body | `string` | yes | Template for the output file if text matches are found. |
| `noTextFileName` | body | `string` | yes | Template for the output file if no text match is found. |
| `zones[]` | body | `array<object>` | no | Text extraction zone objects with location, expression, position, and optional regex. |
