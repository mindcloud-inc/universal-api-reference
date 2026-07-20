# Get a Markdown Document with Veryfi

Retrieves a markdown document from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/document-to-markdown/:document_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get a Markdown Document](https://docs.veryfi.com/api/document-to-markdown/get-a-markdown-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `bounding_boxes` | query | `boolean` | no | A field used to determine whether or not to return bounding_box and bounding_region for extracted fields in the Document response. |
| `confidence_details` | query | `boolean` | no | A field used to determine whether or not to return the score and ocr_score fields in the Document response. |
