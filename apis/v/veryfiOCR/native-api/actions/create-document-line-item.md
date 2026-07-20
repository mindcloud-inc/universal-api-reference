# Create Document Line Item with Veryfi OCR

Creates a document line item in Veryfi OCR.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/documents/:document_id/line-items`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Create Document Line Item](https://docs.veryfi.com/api/receipts-invoices/create-a-line-item/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
