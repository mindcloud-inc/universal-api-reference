# Shuffle PDF Files with PDFCrowd

Creates one PDF by shuffling PDF pages in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Shuffle PDF Files](https://pdfcrowd.com/api/pdf-to-pdf-http/ref/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `f_1` | body | `file` | yes | First PDF file to shuffle. |
| `f_2` | body | `file` | yes | Second PDF file to shuffle. |
| `f_3` | body | `file` | no | Optional third PDF file to shuffle. |
| `f_4` | body | `file` | no | Optional fourth PDF file to shuffle. |
