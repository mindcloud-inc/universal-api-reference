# Convert Image File to Image with PDFCrowd

Creates an image from an image file in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert Image File to Image](https://pdfcrowd.com/api/image-to-image-http/ref/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image file to upload and convert into another image format. |
| `output_format` | body | `string` | no | Image output format such as png, jpg, webp, gif, or tiff. |
