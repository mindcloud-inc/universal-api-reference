# List Incident Types with FireHydrant

Retrieves incident types from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/incident_types`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Incident Types](https://docs.firehydrant.com/reference/list_incident_types)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search incident types by name. |
