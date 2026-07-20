# Convert PDF To DOCX with PDF-app

Creates a DOCX file from a PDF in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf_to_docx2`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Convert PDF To DOCX](https://pdf-app.net/apidocumentation?type=pdf_to_docx2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the PDF file to convert to DOCX. |
| `async` | body | `boolean` | no | Set true to queue the conversion asynchronously. |
| `fileName` | body | `string` | no | Optional output file name for the DOCX file. |
