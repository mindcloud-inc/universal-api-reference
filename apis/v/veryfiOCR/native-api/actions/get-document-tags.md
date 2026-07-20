# Get Document Tags with Veryfi OCR

Retrieves document tags from Veryfi OCR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/documents/:document_id/tags`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Get Document Tags](https://docs.veryfi.com/api/receipts-invoices/add-a-tag-to-a-document/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
