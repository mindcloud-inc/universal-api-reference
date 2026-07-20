# Get Document Line Items with Veryfi OCR

Retrieves document line items from Veryfi OCR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/documents/:document_id/line-items`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Get Document Line Items](https://docs.veryfi.com/api/receipts-invoices/get-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
