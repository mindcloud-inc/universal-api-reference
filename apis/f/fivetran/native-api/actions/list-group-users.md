# List Group Users with Fivetran

Retrieves users for a group in Fivetran.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/[:groupId]/users`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [List Group Users](https://fivetran.com/docs/rest-api/api-reference/group)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Return only enabled users when true. |
| `groupId` | path | `string` | yes | The unique identifier for the group within Fivetran. |
