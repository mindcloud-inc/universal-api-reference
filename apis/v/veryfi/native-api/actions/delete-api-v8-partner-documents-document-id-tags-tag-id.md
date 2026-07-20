# Unlink a Tag from a Document with Veryfi

Deletes a tag from a document in Veryfi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v8/partner/documents/:document_id/tags/:tag_id`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Unlink a Tag from a Document](https://docs.veryfi.com/api/receipts-invoices/unlink-a-tag-from-a-document/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document_id` | path | `string` | yes |
| `tag_id` | path | `string` | yes |
