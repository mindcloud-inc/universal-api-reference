# Combine PDF Files with PDFCrowd

Creates one PDF from multiple PDF files in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Combine PDF Files](https://pdfcrowd.com/api/pdf-to-pdf-http/ref/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `f_1` | body | `file` | yes | First PDF file to combine. |
| `f_2` | body | `file` | yes | Second PDF file to combine. |
| `f_3` | body | `file` | no | Optional third PDF file to combine. |
| `f_4` | body | `file` | no | Optional fourth PDF file to combine. |
