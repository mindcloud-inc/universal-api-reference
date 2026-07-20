# Convert PDF File to Image with PDFCrowd

Creates an image from a PDF file in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert PDF File to Image](https://pdfcrowd.com/api/pdf-to-image-http/ref/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | PDF file to upload and convert into an image file. |
| `output_format` | body | `string` | no | Image output format such as png, jpg, webp, gif, or tiff. |
