# Get Sales Invoice Details with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/getinvoice`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Get Sales Invoice Details](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/get-invoice-details/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | Sales invoice ID from Merit docs. |
| `AddAttachment` | body | `boolean` | no | Include attachment file content when true. |
