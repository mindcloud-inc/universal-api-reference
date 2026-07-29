# List Invoices Missing Payment Date with Rillion Prime Web Service

List invoices that have no payment date registered in Prime.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Company` | body | `list<string>` | no | Company ID to scope the call. |
| `FromAccountCodingDate` | body | `string` | yes | Only include invoices with accounting date on or after this date (yyyy-MM-dd). The server rejects the call without it (verified live). |
| `ERP` | body | `string` | no | ERP identifier to filter by. |
