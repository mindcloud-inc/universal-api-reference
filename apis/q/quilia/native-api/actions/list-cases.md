# List Cases with Quilia

## Endpoint

- **Method:** `GET`
- **Path:** `cases`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [List Cases](https://api.quilia.dev/v2#tag/cases/GET/cases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[client_id]` | query | `string` | no | Filter by client_id. See endpoint description for syntax. |
| `filter[client_name]` | query | `string` | no | Filter by client_name. See endpoint description for syntax. |
| `filter[status]` | query | `string` | no | Filter by status. See endpoint description for syntax. |
| `filter[type]` | query | `string` | no | Filter by type. See endpoint description for syntax. |
