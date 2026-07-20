# Get text from PDF with Aquaforest PDF

Retrieves matched text from PDFs in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/GetTextValue`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [Get text from PDF](https://learn.microsoft.com/en-us/connectors/aquaforest/#get-text-from-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | The content of the source PDF file. |
| `sourceFileName` | body | `string` | yes | The name of the source file. |
| `textResultTemplate` | body | `string` | yes | Template for the text returned when a match is found. |
| `noTextTemplate` | body | `string` | yes | Template for the text returned when no match is found. |
| `pagerange` | body | `string` | no | Page range to extract text from, such as 1,2,4-7. |
| `zones[]` | body | `array<object>` | no | Text extraction zone objects with location, expression, position, and optional regex. |
