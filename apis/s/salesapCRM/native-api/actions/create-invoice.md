# Create Invoice with SalesapCRM

Creates an invoice in SalesapCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://app.salesap.ru/api/v1`
- **Official documentation:** [Create Invoice](https://api.salesap.ru/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API data object for an invoice, including type, attributes, and optional relationships. |
