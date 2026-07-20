# List Group Users with Blaze AI

Retrieves users from a Blaze AI group.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/groups/:group_id/users`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Group Users](https://api.blaze.ai/api/documentation#!/users/getApiV1WWorkspaceIdGroupsGroupIdUsers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `group_id` | path | `number` | yes |
