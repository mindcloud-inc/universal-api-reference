# List Invoices with Bexio

Retrieves invoices from Bexio.

## Endpoint

- **Method:** `GET`
- **Path:** `/2.0/kb_invoice`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [List Invoices](https://docs.bexio.com/#tag/Invoices/operation/v2ListInvoices)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_by` | query | `list<string>` | no | Defines the order of the results. Multiple sort parameters can be combined with a comma separator. `_asc` and `_desc` can be appended to any parameter to sort ascending or descending. Accepted values: `id`, `total`, `total_gross`, `total_net`, `updated_at`. |
