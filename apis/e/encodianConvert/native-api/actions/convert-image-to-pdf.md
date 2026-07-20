# Convert - Image to PDF with Encodian - Convert

Creates a PDF file from an image in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertImageToPdf`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - Image to PDF](https://support.encodian.com/hc/en-gb/articles/23601928355228)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ocrTypeParameter` | query | `string` | no | Set the OCR type to apply when converting an image to PDF. |
| `fileContent` | body | `file` | yes | The file content of the source image. |
