# Delete All Document Line Items with Veryfi OCR

Deletes all document line items from Veryfi OCR.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v8/partner/documents/:document_id/line-items`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Delete All Document Line Items](https://docs.veryfi.com/api/receipts-invoices/get-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
