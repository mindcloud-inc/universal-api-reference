# Search Invoice Payments with Trolley

Finds invoice payments in Trolley using search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/invoices/payment/search`
- **Base URL:** `https://api.trolley.com`
- **Official documentation:** [Search Invoice Payments](https://developers.trolley.com/api/#search-invoice-payments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceIds` | body | `list<string>` | no | Invoice IDs |
