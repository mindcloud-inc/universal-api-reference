# Unlink Tag From Document with Veryfi OCR

Unlinks a tag from a document in Veryfi OCR.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v8/partner/documents/:document_id/tags/:tag_id`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Unlink Tag From Document](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
| `tag_id` | path | `string` | yes | The Veryfi tag identifier. |
