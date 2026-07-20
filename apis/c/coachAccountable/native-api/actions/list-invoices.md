# List Invoices with CoachAccountable

Retrieves invoices from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Invoices](https://www.coachaccountable.com/APIDocs#Invoice.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | Filter invoices by client. If this and CompanyID are omitted, invoices for all invoicees are returned. |
| `CompanyID` | body | `number` | no | Filter invoices by Company. If this and ClientID are omitted, invoices for all invoicees are returned. |
| `dateFrom` | body | `date` | no | Set to restrict Invoices returned to those at or after the provided value. |
| `dateTo` | body | `date` | no | Set to restrict Invoices returned to those at or before the provided value. |
| `sortField` | body | `list` | no | Accepted values: `dateAdded`, `dateDue`, `dateOf`. |
| `sortDirection` | body | `list` | no | Accepted values: `A`, `D`. |
