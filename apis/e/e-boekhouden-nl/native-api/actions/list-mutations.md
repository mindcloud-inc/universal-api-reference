# List Mutations with e-Boekhouden.nl

Retrieves mutations from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/mutation`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Mutations](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `type` | query | `number` | no | Only retrieves mutations of this type. |
| `id` | query | `number` | no | Only retrieves mutations with this number. |
| `description` | query | `string` | no | Only retrieves mutations with this description. |
| `invoiceNumber` | query | `string` | no | Only retrieves mutations with this invoice number. |
| `date` | query | `date` | no | Only retrieves mutations with this date. |
