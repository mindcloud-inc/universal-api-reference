# List Sales Invoices with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/getinvoices`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [List Sales Invoices](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/get-list-of-invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PeriodStart` | body | `string` | yes | Start date in YYYYmmdd from Merit docs. |
| `PeriodEnd` | body | `string` | yes | End date in YYYYmmdd from Merit docs. |
| `DateType` | body | `number` | no | 0=document date, 1=changed date. |
| `UnPaid` | body | `boolean` | no | Filter unpaid invoices only. |
