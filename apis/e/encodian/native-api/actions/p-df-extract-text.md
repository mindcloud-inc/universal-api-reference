# PDF Extract Text with Encodian

Extracts text from a PDF in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/GetPdfTextLayer`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Extract Text](https://support.encodian.com/hc/en-gb/articles/360015539373)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | The PDF filename including the file extension |
| `fileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed |
| `startPage` | body | `number` | no | Sets the page number to begin text extraction from |
| `endPage` | body | `number` | no | Sets the page number to end text extraction from |
| `removeControlCharacters` | body | `boolean` | no | Set whether control characters should be removed from the extracted text |
| `encodingType` | body | `string` | no | Sets the encoding type used for text extraction |
| `returnFile` | body | `boolean` | no | Set whether the action should return a file or alternatively an operation ID |
