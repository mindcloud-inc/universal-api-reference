# Get Invoice with Evoliz

Retrieves an invoice from Evoliz.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/invoices/:invoiceid`
- **Base URL:** `https://www.evoliz.io`
- **Official documentation:** [Get Invoice](https://evoliz.io/documentation#tag/Invoice/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1invoices~1%7Binvoiceid%7D/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoiceid` | path | `number` | yes | The Evoliz invoice ID. |
