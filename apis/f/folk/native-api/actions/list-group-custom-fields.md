# List Group Custom Fields with folk

Retrieves group custom fields for an entity type in folk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/groups/:groupId/custom-fields/:entityType`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [List Group Custom Fields](https://developer.folk.app/api-reference/groups/list-group-custom-fields)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | The entity type for the group's custom fields, such as person or company. |
| `groupId` | path | `string` | yes | The ID of the group whose custom fields you want to list. |
