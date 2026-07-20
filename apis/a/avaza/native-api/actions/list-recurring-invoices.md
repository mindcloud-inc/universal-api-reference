# List Recurring Invoices with Avaza

Retrieves recurring invoices from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/RecurringInvoice`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Recurring Invoices](https://api.avaza.com/#!/RecurringInvoice/RecurringInvoice_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no |
| `CompanyIDFK` | query | `number` | no |
