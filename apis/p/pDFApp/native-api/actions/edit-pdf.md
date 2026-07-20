# Edit PDF with PDF-app

Updates a PDF with edits in PDF-app.

## Endpoint

- **Method:** `POST`
- **Path:** `/edit_pdf`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Edit PDF](https://pdf-app.net/apidocumentation?type=edit_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | PDF file URL to edit. |
| `async` | body | `boolean` | no | Whether to run PDF editing asynchronously. |
| `annotations[]` | body | `array<object>` | no | Text annotations to add to the PDF. |
| `images[]` | body | `array<object>` | no | Images to insert into the PDF. |
| `remove_elements[]` | body | `array<object>` | no | Regions to clear from the PDF. |
| `search_texts[]` | body | `array<object>` | no | Search-and-replace operations for text in the PDF. |
| `fileName` | body | `string` | no | Desired file name for the edited PDF output. |
| `deletePages[]` | body | `array<number>` | no | Page numbers to delete from the PDF. |
| `moveContent[]` | body | `array<object>` | no | Content transformations to apply to rectangular areas of the PDF. |
