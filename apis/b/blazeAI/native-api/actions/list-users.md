# List Users with Blaze AI

Retrieves users from a Blaze AI workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspace_id/users`
- **Base URL:** `https://api.blaze.ai`
- **Official documentation:** [List Users](https://api.blaze.ai/api/documentation#!/users/getApiV1WWorkspaceIdUsers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
