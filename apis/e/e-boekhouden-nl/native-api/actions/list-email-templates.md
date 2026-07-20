# List Email Templates with e-Boekhouden.nl

Retrieves email templates from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/emailtemplate`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Email Templates](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
