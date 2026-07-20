# List Institution Locations with FDIC

Retrieves institution locations from FDIC.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations`
- **Base URL:** `https://api.fdic.gov/banks`
- **Official documentation:** [List Institution Locations](https://api.fdic.gov/banks/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Elastic Search query string filter for location records, for example STALP:IA. |
| `fields` | query | `string` | no | Comma-delimited uppercase FDIC fields to include in the response. |
