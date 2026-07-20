# List Group Connections with Fivetran

Retrieves connections for a group in Fivetran.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/[:groupId]/connections`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [List Group Connections](https://fivetran.com/docs/rest-api/api-reference/group)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier for the group within Fivetran. |
| `schema` | query | `string` | no | Filter group connections by schema name. |
