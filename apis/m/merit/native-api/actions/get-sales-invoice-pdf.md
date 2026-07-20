# Get Sales Invoice PDF with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/getsalesinvpdf`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Get Sales Invoice PDF](https://api.merit.ee/connecting-robots/reference-manual/sales-invoices/create-sales-invoice/get-sales-invoice-pdf/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | Sales invoice ID from Merit docs. |
| `DelivNote` | body | `boolean` | no | If true, generate delivery note without prices. |
