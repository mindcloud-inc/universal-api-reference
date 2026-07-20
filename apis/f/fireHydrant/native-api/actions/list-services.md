# List Services with FireHydrant

Retrieves services from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/services`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Services](https://docs.firehydrant.com/reference/list_services)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `impacted` | query | `string` | no | Filter by whether services are impacted by active incidents. |
| `name` | query | `string` | no | Search services by name. |
| `owner` | query | `string` | no | Filter by owning team ID. |
| `query` | query | `string` | no | Search services by name or description. |
