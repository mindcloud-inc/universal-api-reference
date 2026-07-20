# List Invoices and Quotations with Synchroteam

Retrieves invoices and quotations from Synchroteam using supported filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/v2/Invoices/List`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [List Invoices and Quotations](https://api.synchroteam.com/v2/#list-invoice-quotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional. Provide the Synchroteam invoice list filters object (per docs). |
