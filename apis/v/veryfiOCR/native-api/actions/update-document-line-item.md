# Update Document Line Item with Veryfi OCR

Updates a document line item in Veryfi OCR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v8/partner/documents/:document_id/line-items/:line_item_id`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Update Document Line Item](https://docs.veryfi.com/api/receipts-invoices/create-a-line-item/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
| `line_item_id` | path | `string` | yes | The Veryfi line item identifier. |
