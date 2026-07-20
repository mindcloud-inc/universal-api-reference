# Get Invoice with FreshBooks

Retrieves an invoice from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/invoices/invoices/:invoiceId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Get Invoice](https://www.freshbooks.com/api/invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `invoiceId` | path | `string` | yes | FreshBooks invoice ID. |
