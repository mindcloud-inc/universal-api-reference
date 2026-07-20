# List Invoices with FreeAgent

Retrieves a list of invoices from FreeAgent.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [List Invoices](https://dev.freeagent.com/docs/invoices#list-all-invoices)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | query | `string` | no | Filter invoices by FreeAgent contact resource URL. |
| `project` | query | `string` | no | Filter invoices by FreeAgent project resource URL. |
| `updated_since` | query | `date` | no | Only return invoices updated after this timestamp. |
| `view` | query | `string` | no | Filter the invoice collection by FreeAgent view. |
