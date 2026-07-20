# List Outstanding Invoices with e-Boekhouden.nl

Retrieves outstanding invoices from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/mutation/invoice/outstanding`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Outstanding Invoices](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `credDeb` | query | `string` | yes | Retrieve creditors (`C`) or debtors (`D`). Maximum length: 1. |
| `invoiceNumber` | query | `string` | no | Only retrieve invoices with this number. |
