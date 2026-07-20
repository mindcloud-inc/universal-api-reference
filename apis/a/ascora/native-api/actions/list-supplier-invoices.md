# List Supplier Invoices with Ascora

Retrieves supplier invoices from Ascora.

## Endpoint

- **Method:** `GET`
- **Path:** `/SupplierInvoices/SupplierInvoices`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [List Supplier Invoices](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=59)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `InvoiceDateEnd` | query | `date` | no | Search for invoices with an Invoice Date on or before the specified date. |
| `InvoiceDateStart` | query | `date` | no | Search for invoices with an Invoice Date on or after the specified date. |
| `SupplierName` | query | `string` | no | Performs a partial match against the Supplier Name. |
| `ToBeSentToAccounting` | query | `boolean` | no | Limits the results returned to only Supplier Invoices that have not been pushed to the Accounting Package yet. |
| `TrackingNumber` | query | `string` | no | Performs a partial match against the Supplier Invoice/Credit Note Number. |
