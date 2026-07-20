# Convert HTML File to Image with PDFCrowd

Creates an image from an HTML file in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert HTML File to Image](https://pdfcrowd.com/api/html-to-image-http/ref/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | HTML file to upload and convert into an image. |
| `output_format` | body | `string` | no | Image output format such as png, jpg, webp, gif, or tiff. |
