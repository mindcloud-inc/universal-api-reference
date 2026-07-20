# List Invoices with e-Boekhouden.nl

Retrieves invoices from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/invoice`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Invoices](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `invoiceNumber` | query | `string` | no | Only retrieve the invoice with this number. |
| `relationId` | query | `number` | no | Only retrieve invoices from this relation. |
| `date` | query | `date` | no | Only retrieve invoices on this date. |
