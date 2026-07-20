# Create PDF From HTML with PDF-app

Creates a PDF from HTML in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/html_to_pdf`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Create PDF From HTML](https://pdf-app.net/apidocumentation?type=html_to_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html_template` | body | `string` | yes | HTML content to render into a PDF. |
| `fileName` | body | `string` | no | Optional output file name. |
| `async` | body | `boolean` | no | Set true to queue the PDF generation asynchronously. |
| `format` | body | `string` | no | Optional paper format such as A4 or Letter. |
| `template_html_id` | body | `string` | no | Optional saved HTML template ID to reuse instead of sending raw HTML. |
