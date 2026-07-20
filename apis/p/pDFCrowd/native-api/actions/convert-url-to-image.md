# Convert URL to Image with PDFCrowd

Creates an image from a URL in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert URL to Image](https://pdfcrowd.com/api/html-to-image-http/ref/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public web page URL to convert into an image. |
| `output_format` | body | `string` | no | Image output format such as png, jpg, webp, gif, or tiff. |
