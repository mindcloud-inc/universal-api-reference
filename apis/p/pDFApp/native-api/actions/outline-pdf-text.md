# Outline PDF Text with PDF-app

Updates a PDF by outlining its text in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf_outline_text`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Outline PDF Text](https://pdf-app.net/apidocumentation?type=pdf_outline_text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | PDF file URL whose text should be converted to outlines. |
