# Convert PDF To Word with Encodian

Converts a PDF document to Word in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertPdfToWord`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert PDF To Word](https://support.encodian.com/hc/en-gb/articles/360027229294)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OutputFilename` | body | `string` | yes | The output Microsoft Word filename including the file extension. |
| `FileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be converted. |
| `ConversionMode` | body | `string` | no | Select the conversion mode to use. |
| `RecognizeBullets` | body | `boolean` | no | Enable or disable the recognition of bullets. |
