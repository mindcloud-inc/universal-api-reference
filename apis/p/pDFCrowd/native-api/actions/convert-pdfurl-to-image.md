# Convert PDF URL to Image with PDFCrowd

Creates an image from a PDF URL in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert PDF URL to Image](https://pdfcrowd.com/api/pdf-to-image-http/ref/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public PDF URL to convert into an image file. |
| `output_format` | body | `string` | no | Image output format such as png, jpg, webp, gif, or tiff. |
