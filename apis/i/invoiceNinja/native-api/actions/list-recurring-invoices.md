# List Recurring Invoices with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/recurring_invoices`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [List Recurring Invoices](https://api-docs.invoicing.co/#tag/Recurring-Invoices/operation/getRecurringInvoices)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `string` | no | Filter by client. |
| `frequency_id` | query | `string` | no | Filter by recurrence frequency. |
| `filter` | query | `string` | no | Free-text filter value. |
