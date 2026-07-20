# Convert DOCX To PDF with PDF-app

Creates a PDF from a DOCX file in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/docx_to_pdf_converter`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Convert DOCX To PDF](https://pdf-app.net/apidocumentation?type=docx_to_pdf_converter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | Public URL of the DOCX file to convert. |
| `async` | body | `boolean` | no | Set true to queue the conversion asynchronously. |
| `fileName` | body | `string` | no | Optional output file name for the converted PDF. |
