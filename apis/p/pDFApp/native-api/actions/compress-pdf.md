# Compress PDF with PDF-app

Creates a compressed PDF in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/compress_PDF`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Compress PDF](https://pdf-app.net/apidocumentation?type=compress_PDF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | Public URL of the PDF to compress. |
| `pdfSettings` | body | `string` | no | Compression profile such as /screen, /ebook, /printer, or /prepress. |
| `async` | body | `boolean` | no | Set true to run compression asynchronously. |
| `fileName` | body | `string` | no | Optional output file name for the compressed PDF. |
| `jpegQuality` | body | `number` | no | Optional JPEG quality setting for image recompression. |
