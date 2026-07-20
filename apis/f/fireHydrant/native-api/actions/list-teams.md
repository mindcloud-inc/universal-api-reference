# List Teams with FireHydrant

Retrieves teams from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Teams](https://docs.firehydrant.com/reference/list_teams)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter teams by name. |
| `query` | query | `string` | no | Search teams by name. |
