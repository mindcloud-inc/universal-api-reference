# List Invoices with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [List Invoices](https://api-docs.invoicing.co/#tag/invoices/operation/getInvoices)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `string` | no | Filter invoices by client id. |
| `filter` | query | `string` | no | Text filter for invoice search. |
| `status` | query | `string` | no | Filter invoices by status values such as active, archived, or deleted. |
