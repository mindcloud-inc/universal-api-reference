# Add Image Watermark with PDF Blocks

Updates a PDF document with an image watermark in PDF Blocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/add_watermark/image`
- **Base URL:** `https://api.pdfblocks.com`
- **Official documentation:** [Add Image Watermark](https://www.pdfblocks.com/docs/api/add-image-watermark-to-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The input PDF document. |
| `image` | body | `file` | yes | The image to add as a watermark. |
| `transparency` | body | `number` | no | The transparency level for the image watermark. |
| `margin` | body | `number` | no | The distance in inches from the border of the page to the image watermark. |
