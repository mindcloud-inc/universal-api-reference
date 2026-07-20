# Convert Image URL to Image with PDFCrowd

Creates an image from an image URL in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert Image URL to Image](https://pdfcrowd.com/api/image-to-image-http/ref/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public image URL to convert into another image format. |
| `output_format` | body | `string` | no | Image output format such as png, jpg, webp, gif, or tiff. |
