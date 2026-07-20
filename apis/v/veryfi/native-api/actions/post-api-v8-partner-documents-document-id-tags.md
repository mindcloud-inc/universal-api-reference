# Add Tags to a Document with Veryfi

Adds tags to a document in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/documents/:document_id/tags`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Add Tags to a Document](https://docs.veryfi.com/api/receipts-invoices/add-tags-to-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | — |
| `tags[]` | body | `array<string>` | yes | Possible values: >= 1 |
