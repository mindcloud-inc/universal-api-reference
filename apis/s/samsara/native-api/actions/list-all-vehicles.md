# List Vehicles with Samsara

## Endpoint

- **Method:** `GET`
- **Path:** `fleet/vehicles`
- **Base URL:** `https://api.samsara.com/`
- **Official documentation:** [List Vehicles](https://developers.samsara.com/reference/listvehicles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAfterTime` | query | `string` | no | Return vehicles created at or after this RFC 3339 timestamp. |
| `updatedAfterTime` | query | `string` | no | Return vehicles updated at or after this RFC 3339 timestamp. |
