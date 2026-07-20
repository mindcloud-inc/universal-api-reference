# List Functionalities with FireHydrant

Retrieves all functionality records from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/functionalities`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Functionalities](https://docs.firehydrant.com/reference/list_functionalities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `impacted` | query | `string` | no | Filter by whether functionalities are impacted by active incidents. |
| `name` | query | `string` | no | Search functionalities by name. |
| `owner` | query | `string` | no | Filter by owning team ID. |
| `query` | query | `string` | no | Search functionalities by name or description. |
