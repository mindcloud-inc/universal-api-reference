# OCR PDF or image to searchable PDF with Aquaforest PDF

Creates a searchable PDF from a PDF or image in Aquaforest PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/OcrFile`
- **Base URL:** `https://aquaforest-pdf.azure-api.net/AquaforestPDFAPIV2`
- **Official documentation:** [OCR PDF or image to searchable PDF](https://learn.microsoft.com/en-us/connectors/aquaforest/#ocr-pdf-or-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `file` | yes | Content of the file to OCR. |
| `fileNameWithExtension` | body | `string` | yes | The source file name with extension, or just the extension with a leading dot. |
| `language` | body | `string` | no | OCR processing language. Default is English. |
| `autorotate` | body | `boolean` | no | Auto rotate the image so text is oriented normally. |
