# Cancel Invoice with Refrens

## Endpoint

- **Method:** `PATCH`
- **Path:** `/businesses/:urlKey/invoices/:invoice`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [Cancel Invoice](https://www.refrens.com/api/docs/invoices/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `invoice` | path | `string` | yes |
| `cancelPayment` | query | `boolean` | no |
