# Search Payable Invoices with Moxie

Finds payable invoices in Moxie.

## Endpoint

- **Method:** `GET`
- **Path:** `/action/payableInvoices/search`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Search Payable Invoices](https://help.withmoxie.com/en/articles/8260252-search-payable-invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Optional client name filter if you only want invoices for a specific client. |
