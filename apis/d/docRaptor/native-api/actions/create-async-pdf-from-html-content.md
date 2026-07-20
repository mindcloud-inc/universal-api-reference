# Create Async PDF from HTML Content with DocRaptor

Creates an async PDF in DocRaptor from HTML content.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs`
- **Base URL:** `https://api.docraptor.com`
- **Official documentation:** [Create Async PDF from HTML Content](https://docraptor.com/documentation/api/async)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_content` | body | `string` | yes | HTML content to convert into an async PDF. |
| `name` | body | `string` | no | Optional output file name. |
| `test` | body | `boolean` | no | Create a watermarked test document instead of a production document. |
| `callback_url` | body | `string` | no | Optional URL DocRaptor should call when the async job completes. |
