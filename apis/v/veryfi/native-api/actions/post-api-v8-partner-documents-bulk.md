# Bulk Process Multiple Documents with Veryfi

Creates multiple documents in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/documents/bulk`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Bulk Process Multiple Documents](https://docs.veryfi.com/api/receipts-invoices/bulk-process-multiple-documents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_urls[]` | body | `array<string>` | yes | Possible values: >= 1 , <= 100 An array of URLs to publicly accessible documents to be sent to Veryfi for processing. |
