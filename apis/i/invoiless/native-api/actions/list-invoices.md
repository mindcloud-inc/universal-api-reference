# List Invoices with Invoiless

Retrieves invoices from Invoiless.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://api.invoiless.com/v1`
- **Official documentation:** [List Invoices](https://docs.invoiless.com/guide/invoices.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search by invoice number, customer name, or tags. |
