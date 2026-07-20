# List Connections with Fivetran

Retrieves connections from your Fivetran account.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [List Connections](https://fivetran.com/docs/rest-api/api-reference/connection)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | query | `string` | no | Filter connections by group ID. |
| `schema` | query | `string` | no | Filter connections by schema name. |
