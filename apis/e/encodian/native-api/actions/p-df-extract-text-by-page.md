# PDF Extract Text By Page with Encodian

Extracts PDF text by page in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PDF/PdfExtractTextByPage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PDF Extract Text By Page](https://support.encodian.com/hc/en-gb/articles/20683984513180)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | A Base64 encoded representation of the PDF file to be processed. |
| `startPage` | body | `number` | no | Sets the page number to begin text extraction from. |
| `endPage` | body | `number` | no | Sets the page number to end text extraction from. |
| `pageNumbers` | body | `string` | no | A comma-separated list of page numbers to extract. |
