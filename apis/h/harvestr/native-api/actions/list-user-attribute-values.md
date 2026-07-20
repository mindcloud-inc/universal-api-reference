# List User Attribute Values with Harvestr.io

## Endpoint

- **Method:** `GET`
- **Path:** `/user/{id}/attribute-value`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [List User Attribute Values](https://developers.harvestr.io/api/list-users-attribute-values/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier (id or clientId) |
| `created_before` | query | `date` | no | Filter items created before this date (ISO 8601 format) |
| `created_after` | query | `date` | no | Filter items created after this date (ISO 8601 format) |
| `updated_before` | query | `date` | no | Filter items updated before this date (ISO 8601 format) |
| `updated_after` | query | `date` | no | Filter items updated after this date (ISO 8601 format) |
