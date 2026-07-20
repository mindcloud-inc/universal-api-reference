# Convert URL to PDF with PDFCrowd

Creates a PDF from a URL in PDFCrowd.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.pdfcrowd.com/convert/24.04/`
- **Base URL:** `https://api.pdfcrowd.com/convert/24.04/`
- **Official documentation:** [Convert URL to PDF](https://pdfcrowd.com/api/html-to-pdf-http/ref/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public web page URL to convert into a PDF. |
| `fail_on_main_url_error` | body | `boolean` | no | Abort the conversion when the main URL returns an HTTP error status. |
| `content_viewport_width` | body | `string` | no | Viewport width used when rendering the page before conversion. |
