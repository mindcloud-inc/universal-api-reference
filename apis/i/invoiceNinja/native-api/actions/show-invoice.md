# Show Invoice with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:id`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Show Invoice](https://api-docs.invoicing.co/#tag/invoices/operation/showInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The invoice hashed id. |
| `include` | query | `string` | no | Comma-separated child relationships to include in the response. |
