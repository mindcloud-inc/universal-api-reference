# List Invoice Templates with e-Boekhouden.nl

Retrieves invoice templates from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/invoicetemplate`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Invoice Templates](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `name` | query | `string` | no | Name of the invoice template. |
| `type` | query | `string` | no | Template type. Editor (`E`) or advanced (`A`). |
| `active` | query | `boolean` | no | Whether the invoice template is active. |
