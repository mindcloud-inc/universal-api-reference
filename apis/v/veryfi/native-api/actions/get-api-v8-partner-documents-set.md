# Get Submitted PDF with Veryfi

Retrieves a submitted PDF from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/documents-set`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get Submitted PDF](https://docs.veryfi.com/api/receipts-invoices/get-submitted-pdf/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Default value: 1 The page number. The response is capped to maximum of 50 results per page. |
| `page_size` | query | `number` | no | Default value: 50 The number of Documents per page. |
