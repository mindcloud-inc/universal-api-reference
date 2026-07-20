# Convert HTML String to Image with PDFCrowd

Creates an image from an HTML string in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert HTML String to Image](https://pdfcrowd.com/api/html-to-image-http/ref/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Raw HTML markup to convert into an image file. |
| `output_format` | body | `string` | no | Image output format such as png, jpg, webp, gif, or tiff. |
