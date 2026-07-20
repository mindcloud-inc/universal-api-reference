# Get Invoice with EenvoudigFactureren

Retrieves an invoice from EenvoudigFactureren.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:invoice_id`
- **Base URL:** `https://eenvoudigfactureren.be/api/v1`
- **Official documentation:** [Get Invoice](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `string` | yes | EenvoudigFactureren invoice ID. |
