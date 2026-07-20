# List Units with e-Boekhouden.nl

Retrieves units from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/unit`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [List Units](https://api.e-boekhouden.nl/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to retrieve. |
| `offset` | query | `number` | no | The number of items to skip. |
| `singular` | query | `string` | no | The singular form for the unit. |
| `plural` | query | `string` | no | The plural form for the unit. |
