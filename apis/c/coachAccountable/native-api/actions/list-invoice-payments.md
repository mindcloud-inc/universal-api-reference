# List Invoice Payments with CoachAccountable

Retrieves invoice payments from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Invoice Payments](https://www.coachaccountable.com/APIDocs#Invoice.getPayments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `date` | no | Set to restrict Invoice Payments returned to those at or after the provided value. |
| `dateTo` | body | `date` | no | Set to restrict Invoice Payments returned to those at or before the provided value. |
| `sortField` | body | `list` | no | Accepted values: `datePaid`, `invoiceNumber`. |
| `sortDirection` | body | `list` | no | Accepted values: `A`, `D`. |
