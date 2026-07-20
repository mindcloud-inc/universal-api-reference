# Convert PDF To Images with PDF-app

Creates image files from a PDF in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf_to_image`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Convert PDF To Images](https://pdf-app.net/apidocumentation?type=pdf_to_image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pdfUrls[]` | body | `array<string>` | yes | Public URLs of the PDF files to convert into images. |
| `imageType` | body | `string` | no | Output image format for the converted pages, such as jpeg or png. |
| `quality` | body | `number` | no | Output image quality from 72 to 400. |
| `async` | body | `boolean` | no | Run the conversion asynchronously and fetch the result later by job ID. |
| `fileName` | body | `string` | no | Optional base filename for the generated image files. |
