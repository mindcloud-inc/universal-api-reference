# List Purchase Invoices with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/getpurchorders`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [List Purchase Invoices](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/get-list-of-purchase-invoices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PeriodStart` | body | `string` | yes | Start date in YYYYmmDD format. |
| `PeriodEnd` | body | `string` | yes | End date in YYYYmmDD format. |
| `UnPaid` | body | `boolean` | no | Whether to return only unpaid documents. |
| `DateType` | body | `number` | yes | 0 for document date, 1 for changed date. |
