# Generate Invoice IRN with Refrens

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:urlKey/invoices/:invoice/irn`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [Generate Invoice IRN](https://www.refrens.com/api/docs/generate-einvoice/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `invoice` | path | `string` | yes |
| `includePaymentDetails` | query | `boolean` | no |
