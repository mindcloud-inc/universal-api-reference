# Create PDF from HTML Content with DocRaptor

Creates a PDF in DocRaptor from HTML content.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs`
- **Base URL:** `https://api.docraptor.com`
- **Official documentation:** [Create PDF from HTML Content](https://docraptor.com/documentation/api/making_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_content` | body | `string` | yes | HTML content to convert into a PDF. |
| `name` | body | `string` | no | Optional output file name. |
| `test` | body | `boolean` | no | Create a watermarked test document instead of a production document. |
