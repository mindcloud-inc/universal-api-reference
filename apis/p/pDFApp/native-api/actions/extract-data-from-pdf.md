# Extract Data From PDF with PDF-app

Retrieves extracted data from a PDF in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract_pdf_to_data_py`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Extract Data From PDF](https://pdf-app.net/apidocumentation?type=extract_pdf_to_data_py)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | yes | Public URL of the PDF file to extract data from. |
| `template_id` | body | `string` | no | Optional extraction template ID. |
| `async` | body | `boolean` | no | Run the extraction asynchronously and fetch the result later by job ID. |
| `content[].name` | body | `string` | no | Label for one extraction region. |
| `content[].rectangle` | body | `string` | no | Rectangle coordinates for one extraction region, for example {65, 69, 196, 21}. |
| `content[].page` | body | `number` | no | Page number for one extraction region. |
