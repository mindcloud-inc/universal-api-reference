# Convert Images To PDF with PDF-app

Creates a PDF from image files in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/image_to_pdf`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Convert Images To PDF](https://pdf-app.net/apidocumentation?type=image_to_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrls[]` | body | `array<string>` | yes | Public image URLs to combine into a PDF in order. |
| `async` | body | `boolean` | no | Set true to queue the conversion asynchronously. |
| `fileName` | body | `string` | no | Optional output file name for the created PDF. |
