# Send Invoice or Quotation with Synchroteam

Creates or updates an invoice or quotation in Synchroteam.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/v2/Invoices/Send`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Send Invoice or Quotation](https://api.synchroteam.com/v2/#send-invoice-quotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | yes | Request body payload for creating or updating an invoice (per docs). |
