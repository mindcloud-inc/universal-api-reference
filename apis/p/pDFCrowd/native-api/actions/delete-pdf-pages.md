# Delete PDF Pages with PDFCrowd

Creates a PDF with selected pages deleted in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Delete PDF Pages](https://pdfcrowd.com/api/pdf-to-pdf-http/ref/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `f_1` | body | `file` | yes | PDF file to delete pages from. |
| `page_range` | body | `string` | yes | Comma-separated page numbers or ranges to delete, for example 1,3-5,last. |
