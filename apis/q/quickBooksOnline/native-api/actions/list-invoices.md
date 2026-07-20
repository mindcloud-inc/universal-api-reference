# List Invoices with QuickBooks Online

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [List Invoices](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/most-commonly-used/invoice#query-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Fixed query used to list invoices. |
