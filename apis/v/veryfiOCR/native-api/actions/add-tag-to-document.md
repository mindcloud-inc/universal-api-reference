# Add Tag To Document with Veryfi OCR

Adds a tag to a document in Veryfi OCR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v8/partner/documents/:document_id/tags`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Add Tag To Document](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
