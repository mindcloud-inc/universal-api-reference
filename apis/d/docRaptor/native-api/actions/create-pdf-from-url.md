# Create PDF from URL with DocRaptor

Creates a PDF in DocRaptor from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs`
- **Base URL:** `https://api.docraptor.com`
- **Official documentation:** [Create PDF from URL](https://docraptor.com/documentation/api/making_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_url` | body | `string` | yes | Public URL of the page DocRaptor should convert. |
| `name` | body | `string` | no | Optional output file name. |
| `test` | body | `boolean` | no | Create a watermarked test document instead of a production document. |
