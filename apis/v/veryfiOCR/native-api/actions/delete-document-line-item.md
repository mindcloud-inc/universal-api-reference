# Delete Document Line Item with Veryfi OCR

Deletes a document line item from Veryfi OCR.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v8/partner/documents/:document_id/line-items/:line_item_id`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Delete Document Line Item](https://docs.veryfi.com/api/receipts-invoices/get-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
| `line_item_id` | path | `string` | yes | The Veryfi line item identifier. |
