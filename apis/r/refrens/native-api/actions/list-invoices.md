# List Invoices with Refrens

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/:urlKey/invoices`
- **Base URL:** `https://api.refrens.com`
- **Official documentation:** [List Invoices](https://www.refrens.com/api/docs/invoices/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$sort[createdAt]` | query | `number` | no | Set to 1 for ascending or -1 for descending. |
| `$sort[invoiceNumber]` | query | `number` | no | Set to 1 for ascending or -1 for descending. |
| `$sort[invoiceDate]` | query | `number` | no | Set to 1 for ascending or -1 for descending. |
