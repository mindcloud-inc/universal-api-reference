# List Recurring Invoices with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/getperinvoices`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [List Recurring Invoices](https://api.merit.ee/connecting-robots/reference-manual/recurring-invoices/get-list-of-recurring-invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PeriodStart` | body | `string` | yes | Start date in YYYYmmDD format. |
| `PeriodEnd` | body | `string` | yes | End date in YYYYmmDD format. |
| `DateType` | body | `number` | yes | 0 for next invoice date, 1 for changed date. |
