# Get Purchase Invoice Details with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/getpurchorder`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Get Purchase Invoice Details](https://api.merit.ee/connecting-robots/reference-manual/purchase-invoices/get-purchase-invoice-details/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | Purchase invoice ID. |
| `FillAccCodes` | body | `boolean` | no | Whether to fill account code details when supported. |
