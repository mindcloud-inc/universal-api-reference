# Convert - PDF to Word with Encodian - Convert

Creates a Word file from a PDF in Encodian - Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/ConvertPdfToWord`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert - PDF to Word](https://support.encodian.com/hc/en-gb/articles/360027229294)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | yes | The filename of the source PDF file. |
| `outputFilename` | body | `string` | yes | The filename of the output DOCX document. |
| `finalOperation` | body | `boolean` | yes | Return the processed file instead of just an Operation ID. |
| `fileContent` | body | `file` | no | PDF file content to convert. |
