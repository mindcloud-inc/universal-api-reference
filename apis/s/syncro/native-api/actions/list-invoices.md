# List Invoices with Syncro

Retrieves a list of invoices from Syncro.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [List Invoices](https://api-docs.syncromsp.com/#/Invoice/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paid` | query | `boolean` | no | Return invoices marked as paid. |
| `unpaid` | query | `boolean` | no | Return invoices marked as unpaid. |
| `ticket_id` | query | `number` | no | Return invoices attached to a specific ticket ID. |
| `since_updated_at` | query | `date` | no | Return invoices updated since the provided date. |
| `page` | query | `number` | no | — |
