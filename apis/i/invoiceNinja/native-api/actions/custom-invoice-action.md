# Custom Invoice Action with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:id/:action`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Custom Invoice Action](https://api-docs.invoicing.co/#tag/invoices/operation/actionInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The invoice hashed id. |
| `action` | path | `string` | yes | Invoice action such as history, clone_to_quote, mark_paid, download, or email. |
